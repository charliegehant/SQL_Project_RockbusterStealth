____________________________________________
>>> DESCRIPTIVE STATISTICS of the FILM TABLE
____________________________________________

SELECT    COUNT(film_id) AS count_film_id,
          MIN(film_id) AS min_film_id,
          MAX(film_id) AS max_film_id,

          COUNT(title) AS count_title,
          COUNT(description) AS count_description,

          COUNT(release_year) AS count_release_year,
          AVG(release_year) AS avg_release_year,
          MIN(release_year) AS min_release_year,
          MAX(release_year) AS max_release_year,

          COUNT(language_id) AS count_language_id,
          MIN(language_id) AS min_language_id,
          MAX(language_id) AS max_language_id,

          COUNT(rental_duration) AS count_rental_duration,
          AVG(rental_duration) AS avg_rental_duration,
          MIN(rental_duration) AS min_rental_duration,
          MAX(rental_duration) AS max_rental_duration,

          COUNT(rental_rate) AS count_rental_rate,
          AVG(rental_rate) AS avg_rental_rate,
          MIN(rental_rate) AS min_rental_rate,
          MAX(rental_rate) AS max_rental_rate,

          COUNT(length) AS count_length,
          AVG(length) AS avg_length,
          MIN(length) AS min_length,
          MAX(length) AS max_length,

          COUNT(replacement_cost) AS count_receplacement_cost,
          AVG(replacement_cost) AS avg_replacement_cost,
          MIN(replacement_cost) AS min_replacement_cost,
          MAX(replacement_cost) AS max_replacement_cost,

          COUNT(rating) AS count_rating,

MODE() WITHIN GROUP (ORDER BY rating) AS modal_rating
FROM film

_________________________________________________
>>> DESCRIPTIVE STATISTICS of the CUSTOMERS TABLE
_________________________________________________

SELECT    COUNT(customer_id) AS count_customer_id,
          MIN(customer_id) AS min_customer_id,
          MAX(customer_id) AS max_customer_id,

          COUNT(store_id) AS count_store_id,
          MIN(store_id) AS min_store_id,
          MAX(store_id) AS max_store_id,
          AVG(store_id) AS avg_store_id,

          COUNT(first_name) AS count_first_name,
          COUNT(last_name) AS count_last_name,
          COUNT(email) AS count_email,

          COUNT(address_id) AS count_address_id,
          MIN(address_id) AS min_address_id,
          MAX(address_id) AS max_address_id,
          AVG(address_id) AS avg_address_id,

          COUNT(activebool) AS count_activebool,

MODE() WITHIN GROUP (ORDER BY activebool) AS modal_activebool
FROM customer