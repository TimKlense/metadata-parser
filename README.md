Yep

Note: not perfect like so...

 {'name': 'unique', 'kwargs': {'column_name': 'customer_id', 'model': "{{ get_where_subquery(ref('customers')) }}"}, 'namespace': None}

 {'name': 'not_null', 'kwargs': {'column_name': 'customer_id', 'model': "{{ get_where_subquery(ref('customers')) }}"}, 'namespace': None}

 {'name': 'unique', 'kwargs': {'column_name': 'customer_id', 'model': "{{ get_where_subquery(ref('stg_customers')) }}"}, 'namespace': None}

 {'name': 'not_null', 'kwargs': {'column_name': 'customer_id', 'model': "{{ get_where_subquery(ref('stg_customers')) }}"}, 'namespace': None}

 {'name': 'unique', 'kwargs': {'column_name': 'order_id', 'model': "{{ get_where_subquery(ref('stg_orders')) }}"}, 'namespace': None}

 {'name': 'not_null', 'kwargs': {'column_name': 'order_id', 'model': "{{ get_where_subquery(ref('stg_orders')) }}"}, 'namespace': None}

 {'name': 'accepted_values', 'kwargs': {'values': ['placed', 'shipped', 'completed', 'return_pending', 'returned'], 'column_name': 'status', 'model': "{{ get_where_subquery(ref('stg_orders')) }}"}, 'namespace': None}

 {'name': 'unique', 'kwargs': {'column_name': 'payment_id', 'model': "{{ get_where_subquery(ref('stg_payments')) }}"}, 'namespace': None}

 {'name': 'not_null', 'kwargs': {'column_name': 'payment_id', 'model': "{{ get_where_subquery(ref('stg_payments')) }}"}, 'namespace': None}

 {'name': 'accepted_values', 'kwargs': {'values': ['credit_card', 'coupon', 'bank_transfer', 'gift_card'], 'column_name': 'payment_method', 'model': "{{ get_where_subquery(ref('stg_payments')) }}"}, 'namespace': None}

 {'name': 'unique', 'kwargs': {'column_name': 'order_id', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}

 {'name': 'not_null', 'kwargs': {'column_name': 'order_id', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}

 {'name': 'not_null', 'kwargs': {'column_name': 'customer_id', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}

 {'name': 'relationships', 'kwargs': {'to': "ref('customers')", 'field': 'customer_id', 'column_name': 'customer_id', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}

 {'name': 'accepted_values', 'kwargs': {'values': ['placed', 'shipped', 'completed', 'return_pending', 'returned'], 'column_name': 'status', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}

 {'name': 'not_null', 'kwargs': {'column_name': 'amount', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}

 {'name': 'not_null', 'kwargs': {'column_name': 'credit_card_amount', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}

 {'name': 'not_null', 'kwargs': {'column_name': 'coupon_amount', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}

 {'name': 'not_null', 'kwargs': {'column_name': 'bank_transfer_amount', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}

 {'name': 'not_null', 'kwargs': {'column_name': 'gift_card_amount', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}

 -----

  {'name': 'relationships', 'kwargs': {'to': "ref('customers')", 'field': 'customer_id', 'column_name': 'customer_id', 'model': "{{ get_where_subquery(ref('orders')) }}"}, 'namespace': None}
 would return relationships	customers	customer_id which seems wrong with model
