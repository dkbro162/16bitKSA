module ksa_16(A,B,Cin,clk,Sum,Cout);

input A,B,clk,Cin;
output Sum,Cout;
wire[15:0] A,B;
wire[15:0] Sum;
wire Cin;
//assign A=16'b1000110100110001;
//assign B=16'b0000111100011101;

wire[15:0] Pi,Gi;
wire[14:0] Pi1,Gi1;
wire[13:0] Pi2,Gi2;
wire[11:0] Pi3,Gi3;
wire[7:0] Gi4;

PG mypg1(A[0],B[0],clk,Pi[0],Gi[0]);
PG mypg2(A[1],B[1],clk,Pi[1],Gi[1]);
PG mypg3(A[2],B[2],clk,Pi[2],Gi[2]);
PG mypg4(A[3],B[3],clk,Pi[3],Gi[3]);
PG mypg5(A[4],B[4],clk,Pi[4],Gi[4]);
PG mypg6(A[5],B[5],clk,Pi[5],Gi[5]);
PG mypg7(A[6],B[6],clk,Pi[6],Gi[6]);
PG mypg8(A[7],B[7],clk,Pi[7],Gi[7]);
PG mypg9(A[8],B[8],clk,Pi[8],Gi[8]);
PG mypg10(A[9],B[9],clk,Pi[9],Gi[9]);
PG mypg11(A[10],B[10],clk,Pi[10],Gi[10]);
PG mypg12(A[11],B[11],clk,Pi[11],Gi[11]);
PG mypg13(A[12],B[12],clk,Pi[12],Gi[12]);
PG mypg14(A[13],B[13],clk,Pi[13],Gi[13]);
PG mypg15(A[14],B[14],clk,Pi[14],Gi[14]);
PG mypg16(A[15],B[15],clk,Pi[15],Gi[15]);


PG2 mypg22(Pi[1],Gi[1],Pi[0],Gi[0],clk,Pi1[0],Gi1[0]);
PG2 mypg23(Pi[2],Gi[2],Pi[1],Gi[1],clk,Pi1[1],Gi1[1]);
PG2 mypg24(Pi[3],Gi[3],Pi[2],Gi[2],clk,Pi1[2],Gi1[2]);
PG2 mypg25(Pi[4],Gi[4],Pi[3],Gi[3],clk,Pi1[3],Gi1[3]);
PG2 mypg26(Pi[5],Gi[5],Pi[4],Gi[4],clk,Pi1[4],Gi1[4]);
PG2 mypg27(Pi[6],Gi[6],Pi[5],Gi[5],clk,Pi1[5],Gi1[5]);
PG2 mypg28(Pi[7],Gi[7],Pi[6],Gi[6],clk,Pi1[6],Gi1[6]);
PG2 mypg29(Pi[8],Gi[8],Pi[7],Gi[7],clk,Pi1[7],Gi1[7]);
PG2 mypg210(Pi[9],Gi[9],Pi[8],Gi[8],clk,Pi1[8],Gi1[8]);
PG2 mypg211(Pi[10],Gi[10],Pi[9],Gi[9],clk,Pi1[9],Gi1[9]);
PG2 mypg212(Pi[11],Gi[11],Pi[10],Gi[10],clk,Pi1[10],Gi1[10]);
PG2 mypg213(Pi[12],Gi[12],Pi[11],Gi[11],clk,Pi1[11],Gi1[11]);
PG2 mypg214(Pi[13],Gi[13],Pi[12],Gi[12],clk,Pi1[12],Gi1[12]);
PG2 mypg215(Pi[14],Gi[14],Pi[13],Gi[13],clk,Pi1[13],Gi1[13]);
PG2 mypg216(Pi[15],Gi[15],Pi[14],Gi[14],clk,Pi1[14],Gi1[14]);

PG2 mypg31(Pi1[1],Gi1[1],Pi[0],Gi[0],clk,Pi2[0],Gi2[0]);
PG2 mypg32(Pi1[2],Gi1[2],Pi1[0],Gi1[0],clk,Pi2[1],Gi2[1]);
PG2 mypg33(Pi1[3],Gi1[3],Pi1[1],Gi1[1],clk,Pi2[2],Gi2[2]);
PG2 mypg34(Pi1[4],Gi1[4],Pi1[2],Gi1[2],clk,Pi2[3],Gi2[3]);
PG2 mypg35(Pi1[5],Gi1[5],Pi1[3],Gi1[3],clk,Pi2[4],Gi2[4]);
PG2 mypg36(Pi1[6],Gi1[6],Pi1[4],Gi1[4],clk,Pi2[5],Gi2[5]);
PG2 mypg37(Pi1[7],Gi1[7],Pi1[5],Gi1[5],clk,Pi2[6],Gi2[6]);
PG2 mypg38(Pi1[8],Gi1[8],Pi1[6],Gi1[6],clk,Pi2[7],Gi2[7]);
PG2 mypg39(Pi1[9],Gi1[9],Pi1[7],Gi1[7],clk,Pi2[8],Gi2[8]);
PG2 mypg310(Pi1[10],Gi1[10],Pi1[8],Gi1[8],clk,Pi2[9],Gi2[9]);
PG2 mypg311(Pi1[11],Gi1[11],Pi1[9],Gi1[9],clk,Pi2[10],Gi2[10]);
PG2 mypg312(Pi1[12],Gi1[12],Pi1[10],Gi1[10],clk,Pi2[11],Gi2[11]);
PG2 mypg313(Pi1[13],Gi1[13],Pi1[11],Gi1[11],clk,Pi2[12],Gi2[12]);
PG2 mypg314(Pi1[14],Gi1[14],Pi1[12],Gi1[12],clk,Pi2[13],Gi2[13]);

PG2 mypg41(Pi2[2],Gi2[2],Pi[0],Gi[0],clk,Pi3[0],Gi3[0]);
PG2 mypg42(Pi2[3],Gi2[3],Pi1[0],Gi1[0],clk,Pi3[1],Gi3[1]);
PG2 mypg43(Pi2[4],Gi2[4],Pi2[0],Gi2[0],clk,Pi3[2],Gi3[2]);
PG2 mypg44(Pi2[5],Gi2[5],Pi2[1],Gi2[1],clk,Pi3[3],Gi3[3]);
PG2 mypg45(Pi2[4],Gi2[6],Pi2[0],Gi2[2],clk,Pi3[4],Gi3[4]);
PG2 mypg46(Pi2[5],Gi2[7],Pi2[1],Gi2[3],clk,Pi3[5],Gi3[5]);
PG2 mypg47(Pi2[6],Gi2[8],Pi2[2],Gi2[4],clk,Pi3[6],Gi3[6]);
PG2 mypg48(Pi2[7],Gi2[9],Pi2[3],Gi2[5],clk,Pi3[7],Gi3[7]);
PG2 mypg49(Pi2[8],Gi2[10],Pi2[4],Gi2[6],clk,Pi3[8],Gi3[8]);
PG2 mypg410(Pi2[9],Gi2[11],Pi2[5],Gi2[7],clk,Pi3[9],Gi3[9]);
PG2 mypg411(Pi2[10],Gi2[12],Pi2[6],Gi2[8],clk,Pi3[10],Gi3[10]);
PG2 mypg412(Pi2[11],Gi2[13],Pi2[7],Gi2[9],clk,Pi3[11],Gi3[11]);

justG myG51(Pi3[4],Gi3[4],Gi[0],clk,Gi4[0]);
justG myG52(Pi3[5],Gi3[5],Gi1[0],clk,Gi4[1]);
justG myG53(Pi3[6],Gi3[6],Gi2[0],clk,Gi4[2]);
justG myG54(Pi3[7],Gi3[7],Gi2[1],clk,Gi4[3]);
justG myG55(Pi3[8],Gi3[8],Gi3[0],clk,Gi4[4]);
justG myG56(Pi3[9],Gi3[9],Gi3[1],clk,Gi4[5]);
justG myG57(Pi3[10],Gi3[10],Gi3[2],clk,Gi4[6]);
justG myG58(Pi3[11],Gi3[11],Gi3[3],clk,Gi4[7]);

post myp1(Pi[0],Cin,clk,Sum[0]);
post myp2(Pi[1],Gi[0],clk,Sum[1]);
post myp3(Pi[2],Gi1[0],clk,Sum[2]);
post myp4(Pi[3],Gi2[0],clk,Sum[3]);
post myp5(Pi[4],Gi2[1],clk,Sum[4]);
post myp6(Pi[5],Gi3[0],clk,Sum[5]);
post myp7(Pi[6],Gi3[1],clk,Sum[6]);
post myp8(Pi[7],Gi3[2],clk,Sum[7]);
post myp9(Pi[8],Gi3[3],clk,Sum[8]);
post myp10(Pi[9],Gi4[0],clk,Sum[9]);
post myp11(Pi[10],Gi4[1],clk,Sum[10]);
post myp12(Pi[11],Gi4[2],clk,Sum[11]);
post myp13(Pi[12],Gi4[3],clk,Sum[12]);
post myp14(Pi[13],Gi4[4],clk,Sum[13]);
post myp15(Pi[14],Gi4[5],clk,Sum[14]);
post myp16(Pi[15],Gi4[6],clk,Sum[15]);
assign Cout=Gi4[7];

endmodule

module PG(A0,B0,clk,P0,G0);

input A0,B0;
input clk;
output reg P0,G0;

always@(posedge clk)
	begin
	if(A0==B0)
	P0<=0;
	else P0<=1;
	
	if(A0&&B0)
	G0<=1;
	else G0<=0;
	end

endmodule

module PG2(PC,GC,PP,GP,clk,NP,NG);
input PC, GC;
input PP, GP;
input clk;
output reg NP, NG;

always@(posedge clk)
	begin
	if(PC&&PP)
	NP<=1;
	else NP<=0;
	
	if ((PC&&GP)||GC)
	NG<=1;
	else NG<=0;
	end

endmodule

module justG(Pcu,Gcu,Gpr,clk,Gn);
input Pcu,Gcu,Gpr,clk;
output reg Gn;

always@(posedge clk)
	begin
	if((Pcu||Gpr)||Gcu)
	Gn<=1;
	else Gn<=0;
	end

endmodule

module post(Pc,Gp,clk,Si);
input Pc,Gp,clk;
output reg Si;

always@(posedge clk)
	begin
	if(Pc==Gp)
	Si<=0;
	else Si<=1;
	end
endmodule
