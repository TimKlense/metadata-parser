parse data

Note: not perfect like so...

{'name': 'accepted_values', 'kwargs': {'values': ['credit_card', 'coupon', 'bank_transfer', 'gift_card'], 'column_name': 'payment_method', 'model': "{{ get_where_subquery(ref('stg_payments')) }}"}, 'namespace': None}

{'name': 'relationships', 'kwargs': {'to': "ref('customers')", 'field': 'customer_id', 'column_name': 'customer_id', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}

 -----

  {'name': 'relationships', 'kwargs': {'to': "ref('customers')", 'field': 'customer_id', 'column_name': 'customer_id', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}
 would return relationships	customers	customer_id which isn't quite right
