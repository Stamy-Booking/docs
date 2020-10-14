# Widgets

Die folgenden javascript files müssen in die Webseite eingebunden werden.

``` html
<script src="https://widgets.stamybooking.com/vendor.js"></script>
<script src="https://widgets.stamybooking.com/stamy-widgets.js"></script>
```

## Shopping Cart

Dieses Widget erscheint in From eines Einkaufswagens.

``` html
<stamy-shopping-cart></stamy-shopping-cart>
```

## Kunden Account

Dieses Widget erscheint in From eines Login-Buttons.
Falls der Kunde nicht eingeloggt ist, erscheint ein Dialog zum Login/Registration.
Falls der Kunde eingeloggt ist, wird bei einem Klick auf das Kundenportal umgeleitet.

``` html
<stamy-account-button portalUrl="/customer"></stamy-account-button>
```

Parameter:
| Attribut     | Mögliche Werte| 
| ------------- |:-------------:|
| portalUrl     | permalink zum Kundenportal |

Dieses Widget ist das Kundenportal.
Es sollte allein auf einer Seite auftauchen.

``` html
<stamy-customer-portal></stamy-customer-portal>
```

## Kursplan

Dieses Widget zeigt den aktuellen Kursplan.

``` html
<stamy-courses-schedule></stamy-courses-schedule>
```

Parameter:
| Attribut     | Beschreibung| 
| ------------- |:-------------:|
| consultantSlug   | permalink des Consultants (Kursplan für den Consultant) |
| serviceProductSlug   | permalink des Services (Kursplan für den Service) |
| roomSlug   | permalink des Raumes (Kursplan für den Raum) |

Die Parameter sind als UND-Filter zu verstehen.

## Booking Button

Mit dem Booking-Button können Kurse und Einzeltermine dem Shopping Cart hinzugefügt werden.

``` html
<stamy-booking-button></stamy-booking-button>
```

Das folgende Attribut entscheidet darüber, ob der Button für Klassen oder Flex-Time Kurse angewendet werden soll
| Attribut    | Beschreibung| 
| ------------- |:-------------:|
| mode      | 'single-course', 'course-series', 'courses', 'flex-time'|
| appointmentId    | id des Kurses |
| appointmentSlug    | Permalink des Kurses (als Alternative zur id) |
| serviceProductId    | id des Services |
| serviceProductSlug    | Permalink des Services (als Alternative zur id) |
| consultantId    | id des Consultants |
| consultantSlug    | Permalink des Consultants (als Alternative zur id) |

### Beispiele:

``` html
<stamy-booking-button mode="single-course" appointmentSlug="some-awesome-course"></stamy-booking-button>
```

``` html
<stamy-booking-button mode="flex-time" serviceProductSlug="some-awesome-service" consultantSlug="some-awesome-teacher"></stamy-booking-button>
```

## Tracking

Platziere das folgende Element irgendwo auf der Seite und 
die relevanten Nutzeraktionen werden getrackt.

``` html
<stamy-tracking></stamy-tracking>
```

# Settings

Das Farbschema und die Schriftart können in der Manage App unter:

Einstellungen > Webauftritt

definiert werden.
