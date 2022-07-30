# ANA-505-Week-4-Activity
Week 4: dplyr package



df_hair_eye_color <- data.frame(HairEyeColor)


head(df_hair_eye_color,10)


install.packages("dplyr")
library(dplyr)


select(df_hair_eye_color, Hair, Sex)


df_select_hairsex <- select(df_hair_eye_color, Hair = Hair, Sex = Sex)


df_select_hairsex <- select(df_select_hairsex, -Sex)


rename(df_hair_eye_color, Gender = Sex)


df_hair_eye_color[,"Gender"] <- NA
df_hair_eye_color


df_filter_male <- filter(df_hair_eye_color, Sex == "Male")
df_filter_male <- select(df_filter_male, Sex)
df_filter_male


group_by(df_hair_eye_color, Sex)

#After you run it, write the total here:592

total=mutate(df_hair_eye_color, total=cumsum(Freq))
total


df_filter_female <- filter(df_hair_eye_color, Sex == "Female")
df_filter_female <- select(df_filter_female, Sex)
df_filter_female


bind_rows(df_filter_male,df_filter_female)


arrange_df_hair_eye_color_by_Eye<- arrange(df_hair_eye_color, desc(Eye))
arrange_df_hair_eye_color_by_Eye

