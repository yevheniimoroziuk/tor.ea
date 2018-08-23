.. _contractTermsStructure:

Структура даних: contractTerms
==============================

.. literalinclude:: js/Contractterms.http
   :language: javascript

.. _contractTerms:

contractTerms
-------------

:type:
  Обов’язково. Єдине можливе значення:lease 

  Тип умов контракту.

:leaseTerms:
  Масив :ref:`leaseTerms`

  Блок, що містить інформацію про термінита особливі умови оренди.

.. _leaseTerms:

leaseTerms
----------

:leaseDuration:
  Durations, обов’язково

  Тривалість оренди 

:taxHolidays:
  Масив :ref:`taxHolidays`, не обов’язково

  Орендні канікули

:escalationClauses:
  :ref:`escalationClauses`, не обов’язково

  Індексація ціни

.. _taxHolidays:

taxHolidays
-----------

:id:
  string, auto-generated, read-only

  Ідентифікатор об’єкту

:taxHolidaysDuration:
  Durations, required

  Тривалість орендних канікул.

:conditions:
  string, required

  Умови на час орендних канікул. Вказується українською.

:conditions_en:
  string, optional

  Умови на час орендних канікул. Вказується англійською.

:conditions_ru:
  string, optional

  Умови на час орендних канікул. Вказується російською.

:value:
  :ref:`value`, обов'язково

  Загальна вартість оренди

.. _value:

Value
-----

:amount:
  decimal, required

  Вартість оренди на час орендних канікул.

:currency:
  string, required

  Валюта вартості оренди на час орендних канікул. Єдине доступне значення UAH

:valueAddedTaxIncluded:
  bool, required

  Факт урахування ПДВ. Допустимі значення: true або false

.. _escalationClauses:

escalationClauses
-----------------

:id:
  string, auto-generated, read-only

  Ідентифікатор об’єкту

:escalationPeriodicity:
  Durations`Time intervals, required

  Періодичність, з якою здійснюватиметься індексування вартості.

:escalationStepPercentageRange:
  decimal, required

  Відсоток, в межах якого здійснюватиметься індексування вартості

:conditions:
  string, required

  Умови проведення індексування. Вказується українською.

:conditions_en:
  string, oprional

  Умови проведення індексування. Вказується англійською.

:conditions_ru:
  string, oprional

  Умови проведення індексування. Вказується російською.

