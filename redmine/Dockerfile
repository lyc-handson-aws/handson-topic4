FROM redmine:5.1.1

# add plugins and themes

RUN  git clone https://github.com/arkhitech/redmine_mentions.git plugins/redmine_mentions && \
git clone https://github.com/makotokw/redmine-theme-gitmike.git public/themes/gitmike && \
git clone https://github.com/mrliptontea/PurpleMine2.git public/themes/PurpleMine2 && \
git clone https://github.com/Nitrino/flatly_light_redmine.git public/themes/flatly_light_redmine && \
chown -R redmine:redmine plugins public/themes && \
bundle install


