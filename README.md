# Когортный анализ retention клиентов интернет-магазина

## Стек:
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=matplotlib&logoColor=white)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge)](https://seaborn.pydata.org/)

## Краткое описание проекта

Удержание клиента было оценено с помощью подсчета месячного retention в оформление заказа с помощью когортного анализа. Было определено соответствие интернет магазина рынку (product/market fit)

## Цели проекта:

1. Проанализировать уровень удержания клиентов в интернет-магазине (retention в оформление заказа)
2. Определить, насколько продукт удовлетворяет потребности клиентов, соответствует рынку (product/market fit - PMF)
3. Подобрать метрики, отражающие ... и проанализировать их динамику в интернет-магазине

## Описание данных

В проекте используются три таблицы из набора данных Olist. 
Они содержат информацию о клиентах, заказах и товарных позициях.

### `olist_customers_dataset.csv`

**Назначение:** информация о клиентах и их адресах доставки.

| Поле | Описание |
|---|---|
| `customer_id` | Идентификатор клиента в рамках заказа |
| `customer_unique_id` | Уникальный идентификатор клиента |
| `customer_zip_code_prefix` | Первые пять цифр почтового индекса |
| `customer_city` | Город доставки |
| `customer_state` | Штат доставки |

---

### `olist_orders_dataset.csv`

**Назначение:** информация о заказах и основных этапах их обработки и доставки.

| Поле | Описание |
|---|---|
| `order_id` | Уникальный идентификатор заказа |
| `customer_id` | Идентификатор клиента, оформившего заказ |
| `order_status` | Статус заказа |
| `order_purchase_timestamp` | Дата и время создания заказа |
| `order_approved_at` | Дата и время подтверждения оплаты |
| `order_delivered_carrier_date` | Дата и время передачи заказа в службу доставки |
| `order_delivered_customer_date` | Дата и время доставки заказа клиенту |
| `order_estimated_delivery_date` | Ожидаемая дата доставки |

---

### `olist_order_items_dataset.csv`

**Назначение:** информация о товарах, входящих в состав заказов, и их стоимости.

| Поле | Описание |
|---|---|
| `order_id` | Идентификатор заказа |
| `order_item_id` | Порядковый номер товарной позиции внутри заказа |
| `product_id` | Идентификатор товара |
| `seller_id` | Идентификатор продавца |
| `shipping_limit_date` | Крайний срок передачи заказа продавцом в службу доставки |
| `price` | Цена товара |
| `freight_value` | Стоимость доставки товара |

## Результаты


