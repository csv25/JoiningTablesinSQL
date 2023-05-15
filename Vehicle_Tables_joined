*BAS 220 Homework 1;

libname BAS220 "/home/u63027572/myfolders";

data out_vehicles_stats;
	set BAS220.vehicles_stats;
run;

data out_vehicles_years;
	set BAS220.vehicles_years;
run;


*SQL merge query;
*a = vehicles_stats;
*b = vehicles_years;
proc sql;
	create table vehicle_summary as
	select 
		   b.record_id,
		   a.make,
		   a.model,
		   mpgData,
		   trany,
		   year,
		   barrels08,
		   cylinders,
		   highway08,
		   highway08U		   
	from BAS220.vehicles_stats as a full join BAS220.vehicles_years as b
	on a.record_id = b.record_id;
quit;

proc print data=vehicle_summary(obs=20);
run;

 
*Step 6 Data Dictionary:
1.	barrels08: annual petroleum consumption in barrels for fuelType1 (1)
2.	trany: transmission
3.	mpgData: has My MPG data see yourMpgVehicle and yourMpgDriverVehicle
4.	highway08: highway MPG for fuelType1 (2), (11)
5.	highway08U: unrounded highway MPG for fuelType1 (2), (3)

Step 7 Variables:
(Qualitative or Quantitative)
(Nominal, Ordinal, Binary, Discrete, or Continuous)

1.	barrels08:	Quantitative,	Continuous 
2.	trany: 		Qualitative,	Nominal
3.	mpgData: 	Qualitative,	Binary 
4.	highway08:	Quantitative,	Discrete 
5.	highway08U:	Quantitative,	Continuous

