Using leaver Excel sheet: Sheet1  shape=(307, 33)

Final combined dataset: n=607, leavers=307, stayers=300
Output saved: /content/wydot_model_outputs/combined_modeling_data_32_items.csv

Evaluating Logistic Regression...

Evaluating Random Forest...

Evaluating XGBoost...

MODEL COMPARISON RESULTS
              model  test_auc  test_pr_auc  test_brier  accuracy  precision  recall    f1  tn  fp  fn  tp  cv_auc_mean  cv_auc_sd  cv_pr_auc_mean  cv_brier_mean  cv_f1_mean  cv_recall_mean
            XGBoost     0.998        0.998       0.017     0.975      0.968   0.984 0.976  58   2   1  61        0.994      0.004           0.995          0.030       0.961           0.941
      Random Forest     0.996        0.997       0.034     0.967      1.000   0.935 0.967  60   0   4  58        0.996      0.003           0.996          0.040       0.951           0.911
Logistic Regression     0.990        0.990       0.045     0.934      0.922   0.952 0.937  55   5   3  59        0.968      0.015           0.978          0.057       0.928           0.916

Saved: /content/wydot_model_outputs/model_comparison_results.csv

SYNTHETIC-SOURCE DETECTION CHECK
model                               Logistic Regression  Random Forest
feature_set                                                           
Centered interaction-only features                0.816          0.975
Eight HR theme means                              0.976          0.987
Raw 32 survey items                               0.990          0.996
Within-profile centered items                     0.972          0.992

Saved: /content/wydot_model_outputs/synthetic_source_detection_results.csv

Running sensitivity scenario: baseline

Running sensitivity scenario: mild_less_favorable_all

Running sensitivity scenario: strong_more_favorable_all

Running sensitivity scenario: compensation_weaker

Running sensitivity scenario: communication_safety_stronger

Running sensitivity scenario: random_perturbation

SIMULATION PROBABILITY SENSITIVITY SUMMARY
                     scenario               model  auc_mean  auc_sd  pr_auc_mean  brier_mean  accuracy_mean  recall_mean  f1_mean          top_theme_mode  compensation_rank_median  compensation_rank_mean  compensation_rank_1_rate
                     baseline Logistic Regression     0.992   0.003        0.993       0.036          0.950        0.952    0.951 Safety and Job Security                     4.000                   3.420                     0.020
                     baseline       Random Forest     0.995   0.002        0.996       0.034          0.964        0.932    0.963 Safety and Job Security                     4.000                   3.420                     0.020
                     baseline             XGBoost     0.998   0.002        0.998       0.016          0.981        0.977    0.981 Safety and Job Security                     4.000                   3.420                     0.020
communication_safety_stronger Logistic Regression     0.997   0.002        0.997       0.024          0.969        0.977    0.970 Safety and Job Security                     4.000                   3.540                     0.000
communication_safety_stronger       Random Forest     0.998   0.001        0.998       0.027          0.976        0.955    0.976 Safety and Job Security                     4.000                   3.540                     0.000
communication_safety_stronger             XGBoost     0.999   0.001        0.999       0.012          0.984        0.984    0.984 Safety and Job Security                     4.000                   3.540                     0.000
          compensation_weaker Logistic Regression     0.993   0.003        0.994       0.034          0.952        0.956    0.953 Safety and Job Security                     3.000                   2.900                     0.120
          compensation_weaker       Random Forest     0.995   0.002        0.996       0.033          0.965        0.934    0.964 Safety and Job Security                     3.000                   2.900                     0.120
          compensation_weaker             XGBoost     0.998   0.002        0.998       0.016          0.981        0.978    0.981 Safety and Job Security                     3.000                   2.900                     0.120
      mild_less_favorable_all Logistic Regression     0.988   0.004        0.989       0.044          0.941        0.948    0.943 Safety and Job Security                     3.000                   2.780                     0.160
      mild_less_favorable_all       Random Forest     0.993   0.002        0.995       0.040          0.963        0.930    0.962 Safety and Job Security                     3.000                   2.780                     0.160
      mild_less_favorable_all             XGBoost     0.997   0.002        0.998       0.020          0.976        0.971    0.976 Safety and Job Security                     3.000                   2.780                     0.160
          random_perturbation Logistic Regression     0.993   0.003        0.994       0.034          0.954        0.959    0.955 Safety and Job Security                     4.000                   3.520                     0.040
          random_perturbation       Random Forest     0.996   0.002        0.997       0.032          0.968        0.939    0.967 Safety and Job Security                     4.000                   3.520                     0.040
          random_perturbation             XGBoost     0.999   0.001        0.999       0.015          0.982        0.978    0.982 Safety and Job Security                     4.000                   3.520                     0.040
    strong_more_favorable_all Logistic Regression     0.996   0.002        0.997       0.026          0.964        0.962    0.964 Safety and Job Security                     4.000                   3.760                     0.000
    strong_more_favorable_all       Random Forest     0.998   0.001        0.998       0.027          0.977        0.956    0.977 Safety and Job Security                     4.000                   3.760                     0.000
    strong_more_favorable_all             XGBoost     0.999   0.001        0.999       0.012          0.985        0.984    0.985 Safety and Job Security                     4.000                   3.760                     0.000

Saved: /content/wydot_model_outputs/simulation_probability_sensitivity_detailed.csv
Saved: /content/wydot_model_outputs/simulation_probability_sensitivity_summary.csv

LOGISTIC REGRESSION COEFFICIENT SIGN CHECK
Positive coefficients: 13; Negative coefficients: 19
WARNING: Many positive coefficients found. Because 4=more favorable, many coefficients should be negative. Check coding and column mapping.
Saved: /content/wydot_model_outputs/html_logistic_model_artifacts.json
Saved: /content/wydot_model_outputs/logistic_regression_coefficients.csv
Saved: /content/wydot_model_outputs/theme_risk_weights_from_lr.csv
