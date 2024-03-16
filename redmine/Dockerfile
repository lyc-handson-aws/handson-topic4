FROM redmine:5.1.1

COPY ./assets/configuration.yml /usr/src/redmine/config/

# add plugins and themes
RUN git clone https://github.com/alphanodes/additionals.git plugins/additionals && \
git clone https://github.com/alphanodes/redmine_saml.git plugins/redmine_saml && \
git clone https://github.com/kontron/redmine_oauth.git plugins/redmine_oauth && \
#knowing issue for oauth
sed -i "/gem 'net-imap', '~> 0.3.1'/d" plugins/redmine_oauth/Gemfile && \
git clone https://github.com/alexmonteiro/Redmine-Monitoring-Controlling.git plugins/redmine_monitoring_controlling && \
git clone https://github.com/makotokw/redmine-theme-gitmike.git public/themes/gitmike && \
git clone https://github.com/mrliptontea/PurpleMine2.git public/themes/PurpleMine2 && \
git clone https://github.com/Nitrino/flatly_light_redmine.git public/themes/flatly_light_redmine && \
git clone https://github.com/arkhitech/redmine_mentions.git && \
chown -R redmine:redmine plugins public/themes && \
bundle install


