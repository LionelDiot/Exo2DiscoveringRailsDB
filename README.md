# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

Answers to my exercice :
3.0.0 :001 > Album.count
3.0.0 :004 >  Track.find_by(title: "White Room").artist
3.0.0 :006 > Track.find_by(duration: 188133).title
3.0.0 :007 > Album.find_by(title: "Use Your Illusion II").artist

3.0.0 :008 > Album.where("title LIKE ?", "%Great%").count
3.0.0 :011 > Album.where("title LIKE ?", "%music%").destroy_all
3.0.0 :012 > Album.where(artist: "AC/DC").count
3.0.0 :014 > Track.where(duration: 158589).count

3.0.0 :017 > puts Track.where(artist: "AC/DC").pluck(:title)
3.0.0 :017 > puts Track.where(album: "Let There Be Rock").pluck(:title)
3.0.0 :026 > puts "Total duration: #{Track.where(album: "Let There Be Rock").sum(:duration)} seconds, Total price: $#{Track.where(album: "Let There Be Rock"
).sum(:price).round(2)}"
3.0.0 :028 > puts "le cout de l'integralité de la discographie de deep purple est : #{Track.where(artist: "Deep Purple").sum(:price).round(2)} dollars."
3.0.0 :029 > Track.where(artist:"Eric Clapton").update(artist: "Britney Spears"