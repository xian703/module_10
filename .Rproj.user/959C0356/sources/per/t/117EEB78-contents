#! TO DO:
#! add a rule for rendering the combined report

#! TO DO:
#! add a rule for building the output of 
#! subproject1/code/01_make_table1.R

#! TO DO:
#! add a rule for building the output of 
#! subproject1/code/02_make_scatter.R

#! TO DO:
#! add a rule for building the output of 
#! subproject2/code/01_models.R

combined_report.html: subproject1/output/table_one.rds subproject1/output/scatterplot.png subproject2/output/both_regression_tables.rds
	Rscript render_combined_report.R

subproject1/output/table_one.rds: 
	Rscript subproject1/code/01_make_table1.R

subproject1/output/scatterplot.png: 
	Rscript subproject1/code/02_make_scatter.R

subproject2/output/both_regression_tables.rds: 
	Rscript subproject2/code/01_models.R



.PHONY: clean
clean:
	rm -f subproject1/output/table_one.rds subproject1/output/scatterplot.png subproject2/output/both_regression_tables.rds combined_report.html
