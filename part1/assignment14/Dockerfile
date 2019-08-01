FROM ruby:2.6.0
WORKDIR /ruby-project
EXPOSE 3000
ENV SECRET_KEY_BASE=somesecretkey
COPY . .
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN bundle install
RUN rake secret
RUN rails db:migrate RAILS_ENV=production
RUN rake assets:precompile
CMD ["rails", "s", "-e", "production"]
