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
  Тривалість , обов’язково

  Тривалість оренди .

:taxHolidays:
  Масив :ref:`taxHolidays`, не обов’язково

  Орендні канікули.

:escalationClauses:
  :ref:`escalationClauses`, не обов’язково

  Індексація ціни.

.. _taxHolidays:

taxHolidays
-----------

:id:
  uuid, автогенерований, тільки для читання

  Ідентифікатор об’єкту.

:taxHolidaysDuration:
  тривалість, обов’язково

  Тривалість орендних канікул.

:conditions:
  рядок, обов’язково для української мови, багатомовний

    Умови на час орендних канікул. Вказується українською.

    * conditions_en - Вказується англійською.

    * conditions_ru - Вказується російською.

:value:
  :ref:`value`, обов'язково

  Загальна вартість оренди

.. _value:

Value
-----

:amount:
  decimal, обов’язково

  Вартість оренди на час орендних канікул.

:currency:
  рядок, обов’язково

  Валюта вартості оренди на час орендних канікул. Єдине доступне значення UAH.

:valueAddedTaxIncluded:
  bool, обов’язково

  Факт урахування ПДВ. Допустимі значення: ``true`` або ``false``.

.. _escalationClauses:

escalationClauses
-----------------

:id:
  uuid, автогенерований, тільки для читання

  Ідентифікатор об’єкту

:escalationPeriodicity:
  тривалість, обов’язково

  Періодичність, з якою здійснюватиметься індексування вартості.

:escalationStepPercentageRange:
  decimal, обов’язково

  Відсоток, в межах якого здійснюватиметься індексування вартості

:conditions:
  рядок, обов’язково для української мови, багатомовний

  Умови проведення індексування. Вказується українською.

    * conditions_en - Вказується англійською.

    * conditions_ru - Вказується російською.
