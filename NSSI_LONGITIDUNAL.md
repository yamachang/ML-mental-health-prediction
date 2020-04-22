NSSI\_Longitidunal
================
Yama Chang

## Clean data for longitidunal data

``` r
## load data
baseline = read_sav('./data/baseline.sav')
baseline_v1 = read_sav('./data/baseline_v1.sav')
wave2 = read_sav('./data/wave2.sav')
wave3 = read_sav('./data/wave3.sav')

baseline = cbind(wave = 1, baseline) %>% janitor::clean_names()
baseline_v1 = cbind(baseline_v1 = 1, baseline_v1) %>% janitor::clean_names()
wave2 = cbind(wave = 2, wave2) %>% janitor::clean_names()
wave3 = cbind(wave = 3, wave3) %>% janitor::clean_names()


## merge datasets from baseline, wave2, wave3
# There are four major ways join dataframes x and y:
# Inner: keeps data that appear in both x and y
# Left: keeps data that appear in x
# Right: keeps data that appear in y
# Full: keeps data that appear in either x or y

# .x: 出現第一次
# .y: 出現第二次
# 無標記: 只出現一次/出現第三次

longitidunal_data = 
  full_join(baseline, wave2, by = "id") %>% 
  full_join(., wave3, by = "id")

longitidunal_data2 = 
  left_join(baseline, wave2, by = "id") %>% 
  left_join(., wave3, by = "id")
```

## NSSI Longitidunal Study

``` r
## Select the data we need as NSSI
# select: 選要的column
# filter: 選要的row
# drop_na: remove rows with missing value
# mutate: change columns or create new ones

NSSI = longitidunal_data %>% 
  select(d81.x:d106.x, birth_sex.x: meps_idi.x, d81.y:d106.y, age.y:cope14, if_ideation:d106z, age:meps_idi.y) 
```
