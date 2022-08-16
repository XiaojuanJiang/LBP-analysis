# LBP-analysis


####plots
res_single <- mr_singlesnp(dat)
res_single <- mr_singlesnp(dat, single_method="mr_meta_fixed")
res_loo <- mr_leaveoneout(dat)
res <- mr(dat, method_list=c("mr_egger_regression", "mr_ivw","mr_weighted_median")) 
p1 <- mr_scatter_plot(res, dat)
p1[[1]]
res_single <- mr_singlesnp(dat)
p2 <- mr_forest_plot(res_single)
p2[[1]]

res_loo <- mr_leaveoneout(dat)
p3 <- mr_leaveoneout_plot(res_loo)
p3[[1]]

res_single <- mr_singlesnp(dat)
p4 <- mr_funnel_plot(res_single)
p4[[1]]
