# LBP-analysis

##### MR plots,export the plots as pdf and then organize them in adobe illustration

res_single <- mr_singlesnp(dat)
res_single <- mr_singlesnp(dat, single_method="mr_meta_fixed")
res_loo <- mr_leaveoneout(dat)
res <- mr(dat, method_list=c("mr_egger_regression", "mr_ivw","mr_weighted_median")) 

####scatter plot
p1 <- mr_scatter_plot(res, dat)
p1[[1]]
res_single <- mr_singlesnp(dat)

####forest plot
p2 <- mr_forest_plot(res_single)
p2[[1]]

####leave one out plot
res_loo <- mr_leaveoneout(dat)
p3 <- mr_leaveoneout_plot(res_loo)
p3[[1]]
res_single <- mr_singlesnp(dat)

####funnel plot
p4 <- mr_funnel_plot(res_single)
p4[[1]]

####Radial MR plot
plot_radial(ivw.model)

#### export all the plots as pdf and then combine them into a single diagram.

####The forest plot was drawn using Prism 9 based on the data  presented in the original ariticle.
