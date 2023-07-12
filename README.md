# Module-5-Challenge

This challenge required us to prepare data, generate summary statistics, create bar charts and pie charts, calculate quartiles, outliers and create boxplots, line charts and scatter plots as well as calculating correlation and regression. 

The following was wriiten with the help of a TA in office hours: 
plt.scatter(scatter_plot['Weight (g)'],scatter_plot['Tumor Volume (mm3)'], color="green")
plt.title('Mouse Weight vs. Average Observed Volume for Capomulin')
plt.xlabel('Weight (g)',fontsize =10)
plt.ylabel('Averag Tumor Volume (mm3)')

(slope, intercept, rvalue, pvalue, stderr)= st.linregress(scatter_plot["Weight (g)"],scatter_plot["Tumor Volume (mm3)"])
regress_values=scatter_plot["Weight (g)"]* slope + intercept
line = f"y = {round(slope, 2)} x + {round(intercept, 2)}"

plt.scatter(scatter_plot["Weight (g)"],scatter_plot["Tumor Volume (mm3)"],color='b')
plt.plot(scatter_plot["Weight (g)"], regress_values, color='red')
plt.annotate(line,(20,38), fontsize=10)
plt.xlabel("Weight (g)")
plt.ylabel("Tumor Volume (mm3)")
plt.title("Weight vs Tumor Volume for Capomulin")
plt.show()
