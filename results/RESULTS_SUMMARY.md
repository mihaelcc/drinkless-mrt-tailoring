# Drink Less MRT — results summary

Runtime: 353.3 s · Env: {'python': '3.13.16', 'numpy': '2.1.3', 'pandas': '2.2.3', 'lightgbm': '4.6.0', 'sklearn': '1.6.1', 'shap': '0.54.1', 'statsmodels': '0.15.0'}

## Descriptives
{"n_user_days": 10470, "n_users": 349, "p_notification": 0.598, "p_standard": 0.297, "p_new": 0.3, "p_open_8_9pm": 0.09, "p_open_if_notified": 0.126, "p_open_if_not": 0.036, "date_first": "2020-01-03", "date_last": "2020-04-30", "weekend_share": 0.285, "age_mean": 43.0, "age_sd": 11.3, "age_range": [21, 71], "female": 0.556, "manual": 0.106, "audit_mean": 17.9, "audit_sd": 6.4, "audit_cat": {"Hazardous (8-15)": 142, "At risk of alcohol dependence (20-40)": 123, "Harmful (16-19)": 84}, "p_used_before_8pm": 0.231, "p_already_engaged": 0.091}

## WCLS (risk difference, open app 8–9 pm)
- marginal: A_c=0.0906 [0.0739, 0.1073], p=0.0000
- day: A_c=0.1459 [0.1184, 0.1735], p=0.0000; A_c:day=-0.0036 [-0.0048, -0.0024], p=0.0000
- day_weekend: A_c=0.1539 [0.1254, 0.1825], p=0.0000; A_c:day=-0.0036 [-0.0048, -0.0024], p=0.0000; A_c:weekend=-0.0283 [-0.0499, -0.0067], p=0.0104
- weekend: A_c=0.0990 [0.0804, 0.1176], p=0.0000; A_c:weekend=-0.0292 [-0.0508, -0.0075], p=0.0083
- before_8pm: A_c=0.0651 [0.0504, 0.0798], p=0.0000; A_c:before_8pm=0.1091 [0.0696, 0.1487], p=0.0000
- already_engaged: A_c=0.0766 [0.0625, 0.0907], p=0.0000; A_c:already_engaged=0.1558 [0.1012, 0.2104], p=0.0000
- after_9pm_day_before: A_c=0.0817 [0.0658, 0.0976], p=0.0000; A_c:after_9pm_day_before=0.0925 [0.0448, 0.1402], p=0.0001
- habituation: A_c=0.0889 [0.0664, 0.1114], p=0.0000; A_c:habituation=0.0027 [-0.0194, 0.0248], p=0.8107
- age: A_c=0.0597 [-0.0051, 0.1244], p=0.0708; A_c:age=0.0007 [-0.0008, 0.0022], p=0.3511
- female: A_c=0.0917 [0.0651, 0.1184], p=0.0000; A_c:female=-0.0020 [-0.0359, 0.0319], p=0.9093
- AUDIT: A_c=0.1076 [0.0567, 0.1584], p=0.0000; A_c:AUDIT_score=-0.0009 [-0.0036, 0.0017], p=0.4791
- type: new_c=0.0857 [0.0673, 0.1041], p=0.0000; std_c=0.0956 [0.0766, 0.1147], p=0.0000

## DR average effect: 0.0897

## By week
{"week": 1, "days": "1-7", "p_notified": 0.1915, "p_not": 0.0464, "rd": 0.145, "rd_lo": 0.1176, "rd_hi": 0.1732, "rr": 4.12, "rr_lo": 3.03, "rr_hi": 5.98}
{"week": 2, "days": "8-14", "p_notified": 0.1364, "p_not": 0.0514, "rd": 0.085, "rd_lo": 0.0605, "rd_hi": 0.1113, "rr": 2.65, "rr_lo": 1.98, "rr_hi": 3.68}
{"week": 3, "days": "15-21", "p_notified": 0.1075, "p_not": 0.0262, "rd": 0.0813, "rd_lo": 0.0595, "rd_hi": 0.1039, "rr": 4.1, "rr_lo": 2.86, "rr_hi": 6.61}
{"week": 4, "days": "22-30", "p_notified": 0.0818, "p_not": 0.0255, "rd": 0.0564, "rd_lo": 0.0382, "rd_hi": 0.0755, "rr": 3.21, "rr_lo": 2.24, "rr_hi": 4.83}
Trend: {'rd_slope_per_week': -0.027, 'rd_lo': -0.0359, 'rd_hi': -0.0177, 'rd_p_ge0': 0.0, 'logrr_slope_per_week': -0.0312, 'logrr_lo': -0.1824, 'logrr_hi': 0.1343}

## Engagement-state moderation
{"variable": "before_8pm", "label": "Used app earlier today", "value": 0, "n": 8047, "rd": 0.0669, "lo": 0.0529, "hi": 0.0809}
{"variable": "before_8pm", "label": "Used app earlier today", "value": 1, "n": 2423, "rd": 0.1722, "lo": 0.1359, "hi": 0.2098}
{"variable": "already_engaged", "label": "Opened app 8\u20139 pm yesterday", "value": 0, "n": 9522, "rd": 0.0761, "lo": 0.0619, "hi": 0.09}
{"variable": "already_engaged", "label": "Opened app 8\u20139 pm yesterday", "value": 1, "n": 948, "rd": 0.2275, "lo": 0.1691, "hi": 0.2844}
{"variable": "after_9pm_day_before", "label": "Used app after 9 pm yesterday", "value": 0, "n": 9469, "rd": 0.0809, "lo": 0.0667, "hi": 0.0974}
{"variable": "after_9pm_day_before", "label": "Used app after 9 pm yesterday", "value": 1, "n": 1001, "rd": 0.1767, "lo": 0.1237, "hi": 0.2263}
{"variable": "habituation", "label": "Notified yesterday", "value": 0, "n": 4179, "rd": 0.0882, "lo": 0.0664, "hi": 0.1126}
{"variable": "habituation", "label": "Notified yesterday", "value": 1, "n": 6291, "rd": 0.0914, "lo": 0.0731, "hi": 0.1094}
{"variable": "weekend", "label": "Weekend", "value": 0, "n": 7487, "rd": 0.0987, "lo": 0.0809, "hi": 0.1182}
{"variable": "weekend", "label": "Weekend", "value": 1, "n": 2983, "rd": 0.0685, "lo": 0.0478, "hi": 0.0896}

## Models (seed 7)
- M1 GBM (context + traits): {'area': 0.0137, 'area_lo': 0.0098, 'area_hi': 0.0173, 'p_area_le0': 0.0, 'g40': 0.0265, 'g40_lo': 0.0194, 'g40_hi': 0.0333, 'g60': 0.0195, 'g60_lo': 0.0134, 'g60_hi': 0.0253, 'cate_sd': 0.0751, 'share_pred_negative': 0.022, 'quartile_effects': [0.0395, 0.0486, 0.1032, 0.1677]}
- M2 GBM (context): {'area': 0.0165, 'area_lo': 0.0129, 'area_hi': 0.0202, 'p_area_le0': 0.0, 'g40': 0.0329, 'g40_lo': 0.025, 'g40_hi': 0.0395, 'g60': 0.0246, 'g60_lo': 0.0187, 'g60_hi': 0.0301, 'cate_sd': 0.0781, 'share_pred_negative': 0.001, 'quartile_effects': [0.035, 0.0401, 0.101, 0.1829]}
- M3 Ridge (context): {'area': 0.0171, 'area_lo': 0.0131, 'area_hi': 0.0206, 'p_area_le0': 0.0, 'g40': 0.0318, 'g40_lo': 0.0245, 'g40_hi': 0.0393, 'g60': 0.0222, 'g60_lo': 0.0165, 'g60_hi': 0.0279, 'cate_sd': 0.0619, 'share_pred_negative': 0.002, 'quartile_effects': [0.0206, 0.0501, 0.1065, 0.1817]}
- M4 Ridge (day + weekend): {'area': 0.0084, 'area_lo': 0.0056, 'area_hi': 0.0109, 'p_area_le0': 0.0, 'g40': 0.0121, 'g40_lo': 0.0078, 'g40_hi': 0.0168, 'g60': 0.0129, 'g60_lo': 0.0088, 'g60_hi': 0.0174, 'cate_sd': 0.0328, 'share_pred_negative': 0.0, 'quartile_effects': [0.0563, 0.073, 0.0946, 0.1351]}
- M5 Random forest (context): {'area': 0.0168, 'area_lo': 0.0129, 'area_hi': 0.0207, 'p_area_le0': 0.0, 'g40': 0.0329, 'g40_lo': 0.025, 'g40_hi': 0.0405, 'g60': 0.0255, 'g60_lo': 0.0193, 'g60_hi': 0.0306, 'cate_sd': 0.0726, 'share_pred_negative': 0.03, 'quartile_effects': [0.0332, 0.0369, 0.1102, 0.1787]}

## Robustness (area by seed)
seed                           7       11      23      101
model                                                     
M1 GBM (context + traits)   0.0137  0.0142  0.0140  0.0137
M2 GBM (context)            0.0165  0.0167  0.0167  0.0168
M3 Ridge (context)          0.0171  0.0173  0.0172  0.0171
M4 Ridge (day + weekend)    0.0084  0.0083  0.0085  0.0081
M5 Random forest (context)  0.0168  0.0169  0.0169  0.0171

## Benefit retained
                              20%    30%    40%    50%    60%    80%
M1 GBM (context + traits)   0.361  0.577  0.696  0.755  0.817  0.906
M2 GBM (context)            0.418  0.590  0.767  0.791  0.874  0.927
M3 Ridge (context)          0.430  0.616  0.755  0.803  0.848  0.949
M4 Ridge (day + weekend)    0.316  0.435  0.535  0.640  0.744  0.871
M5 Random forest (context)  0.424  0.581  0.767  0.805  0.884  0.917

## Rule M3: {'intercept': 0.1076, 'coefs': {'day': -0.0024, 'weekend': -0.0247, 'before_8pm': 0.0782, 'after_9pm_day_before': 0.0608, 'already_engaged': 0.1164, 'habituation': -0.0117}, 'threshold_40pct': 0.0858, 'notified_share_by_state': {'before_8pm': {'0': 0.223, '1': 0.99}, 'already_engaged': {'0': 0.341, '1': 1.0}, 'weekend': {'0': 0.439, '1': 0.305}}}
## Rule M4: {'intercept': 0.1537, 'coefs': {'day': -0.00359, 'weekend': -0.02663}, 'threshold_40pct': 0.1007, 'last_weekday': 14, 'last_weekend': 7}
## SHAP M1 (traits share 0.245): {'before_8pm': 0.02781, 'already_engaged': 0.02025, 'day': 0.0184, 'age': 0.01707, 'after_9pm_day_before': 0.01214, 'AUDIT_score': 0.01062, 'weekend': 0.00837, 'habituation': 0.00446, 'female': 0.00169, 'manual': 0.00033}
## Equity: {'by_engagement_tertile': [{'engagement_tertile': 'Low', 'share_notified_M3': 0.161, 'share_notified_random': 0.61}, {'engagement_tertile': 'Middle', 'share_notified_M3': 0.284, 'share_notified_random': 0.588}, {'engagement_tertile': 'High', 'share_notified_M3': 0.755, 'share_notified_random': 0.595}], 'users_zero_notifications_days17_30': 0.493}