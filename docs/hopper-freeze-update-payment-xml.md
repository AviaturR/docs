---
title: Hopper freeze update payment xml
slug: /hopper-freeze-update-payment-xml
---

## Introducción

xml de add product data oficial:

```xml
<soapenv:Envelope
	xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
	xmlns:ns="http://www.aviatur.com/soa/formato/mbus/request/version/1.0">
	<soapenv:Header/>
	<soapenv:Body>
		<ns:mbus>
			<ns:request>
				<ns:header>
					<ns:service>REGISTRAR_PAGOSPRODSOLIC</ns:service>
					<ns:invoker>BPM</ns:invoker>
					<ns:provider>dummy|http://www.aviatur.com.co/dummy/</ns:provider>
					<ns:requestId>1</ns:requestId>
				</ns:header>
				<ns:body>
					<FILTRO>
						<data>
							<client_id>183282</client_id>
							<order_id>15968042</order_id>
							<operation_id>UPDATE</operation_id>
							<products>
								<product>
									<id>34909283</id>
									<source_id>9VVJE558</source_id>
									<booking_id>9VVJE558</booking_id>
									<booking_id2/>
									<payment_currency>
										<code>COP</code>
									</payment_currency>
									<payment_data>
										<cardholder>yared toro</cardholder>
										<payment_gateway>placetopay</payment_gateway>
										<reference_id>ON1800102-PN1799056</reference_id>
										<card_number>T0000000001658691111</card_number>
										<expired_year>2023</expired_year>
										<expired_month>10</expired_month>
										<approval_code>000000</approval_code>
										<approval_date>2021-09-08 19:56</approval_date>
										<administrative_approval_code></administrative_approval_code>
										<payment_id>2</payment_id>
										<base_amount>0</base_amount>
										<tax_amount>0</tax_amount>
										<total_amount>131123</total_amount>
										<administrative_base>0</administrative_base>
										<administrative_tax>0</administrative_tax>
										<administrative_amount>0</administrative_amount>
										<notes/>
										<extra1/>
										<extra2/>
										<ip_address>190.65.109.65</ip_address>
										<ip_address_city_code>BOG</ip_address_city_code>
										<payment_type>
											<id>1</id>
											<name>Tarjeta de credito</name>
										</payment_type>
										<franchise>
											<code>VS</code>
											<name>Visa</name>
										</franchise>
										<bank>
											<id>CR_VS</id>
											<name>BANCO DE PRUEBAS</name>
										</bank>
										<state>
											<id>1</id>
											<name>Aprobada</name>
											<reason_code>00</reason_code>
											<reason_text/>
										</state>
										<admnistrative_state>
											<id></id>
											<name></name>
											<reason_code></reason_code>
											<reason_text></reason_text>
										</admnistrative_state>
									</payment_data>
								</product>
							</products>
						</data>
					</FILTRO>
				</ns:body>
			</ns:request>
		</ns:mbus>
	</soapenv:Body>
</soapenv:Envelope>

```
