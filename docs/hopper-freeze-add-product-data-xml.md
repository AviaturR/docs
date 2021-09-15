---
title: Hopper add product data xml
slug: /hopper-add-product-data-xml
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
					<ns:service>CREA_SOLICITUD_PRODUCTO</ns:service>
					<ns:invoker>BPM</ns:invoker>
					<ns:provider>dummy|http://www.aviatur.com.co/dummy/</ns:provider>
					<ns:requestId>-691267543</ns:requestId>
				</ns:header>
				<ns:body>
					<FILTRO>
						<data>
							<operation_id>create</operation_id>
							<ref_externa/>

							<transaction_id>eyJlIjoiMTYzMTE1NTg4OV81RjIwIn0.DFu6og6aJ_H-X1aPNl4oKHZ_v9L8Om0VTbJ66f_DCPo</transaction_id>
							<client>
								<id>183282</id>
								<name>yared nicolas</name>
								<last_name>toro </last_name>
							</client>
							<connection_data>
								<ip>190.65.109.65</ip>
								<loc>4.6097,-74.0817</loc>
								<country>CO</country>
								<city>Bogota</city>
								<connection_info>{"ip":"190.65.109.65","city":"Bogota","region":"Bogota D.C.","country":"CO","loc":"4.6097,-74.0817","org":"AS3816 COLOMBIA TELECOMUNICACIONES S.A. ESP","postal":"111411","timezone":"America\/Bogota"}</connection_info>
							</connection_data>
							<sale_freelance/>
							<sale_operator>
								<id/>
								<name/>
								<last_name/>
							</sale_operator>
							<sale_consultant>
								<id/>
								<name/>
								<last_name/>
							</sale_consultant>
							<channel>
								<id>B2C</id>
								<name>B2C</name>
							</channel>
							<office>
								<id>010-0501024</id>
								<name>010-0501024</name>
							</office>
							<state>
								<id>6</id>
								<name>Reserva Realizada</name>
								<notes/>
								<sale_operator>
									<id/>
									<name/>
									<last_name/>
								</sale_operator>
							</state>
							<product>
								<name>Hopper</name>
								<source_id>999</source_id>
								<bill_number>9VVJE558</bill_number><!-- reserva de hopper -->
								<booking_id>9VVJE558</booking_id><!-- reserva de hopper -->
								<booking_id2></booking_id2>
								<booking_date>2021-09-08 19:56</booking_date>
								<booking_date2/>
								<duration_type>D</duration_type>
								<begin_date>2021-04-16 10:05</begin_date><!-- fecha del congelamiento -->
								<end_date>2021-04-22 10:05</end_date><!-- fecha del mxima de regreso a la compra -->
								<stock>1</stock>
								<deposit_allowed/>
								<maximum_payment_date/>
								<minimun_value_cop>0</minimun_value_cop>
								<minimun_value_quote>0</minimun_value_quote>
								<project_billing>0222002</project_billing> <!-- proyecto para contabilidad -->
								<product_type>
									<id>20</id><!-- tipo de producto -->
									<name>Hopper freeze</name> <!-- concepto varios  -->
								</product_type>
								<state>
									<id>6</id>
									<name>Reserva Realizada</name>
									<notes/>
									<sale_operator>
										<id/>
										<name/>
										<last_name/>
									</sale_operator>
								</state>
								<provider>
									<id>999</id> <!-- impotante envia el 999 para hopper -->
									<name>Hopper</name>
								</provider>
								<passenger_types>
									<passenger_type>
										<id>ADT</id>
										<name>Adulto</name>
										<fare>
											<base_amount>0</base_amount>
											<administrative_amount>1</administrative_amount>
											<qse_amount>2</qse_amount>
											<taxes></taxes>
										</fare>
									</passenger_type>
								</passenger_types>
								<passengers_numbers>1</passengers_numbers>
								<passengers>
									<passenger>
										<passenger_number>1</passenger_number>
										<type>ADT</type>
										<first_name>yared nicolas</first_name>
										<second_name/>
										<first_last_name>toro </first_last_name>
										<second_last_name/>
										<document_type>
											<id>CC</id>
											<name>C&#xE9;dula De Ciudadan&#xED;a</name>
										</document_type>
										<document_number>1018505042</document_number>
										<phone_number>3212833647</phone_number>
										<mobile_phone_number>3212833647</mobile_phone_number>
										<birth_date>1998-08-23</birth_date>
										<nationality>CO</nationality>
										<notes/>
										<treatment/>
										<gender_id>335</gender_id>
										<redress_number/>
										<email>yared.toro@aviatur.com</email>
										<address>Cra 79a calle 26 55 sur</address>
										<country_id>BOGOTA</country_id>
										<city_id>CO</city_id>
										<reference/>
										<seats/>
									</passenger>
								</passengers>
								<notes>{product_notes}</notes>
								<fare_currency>
									<code>USD</code><!-- debe ir USD por indicacion de boti -->
									<name>Dolar Estadounidense</name>
									<symbol>USD</symbol>
								</fare_currency>
								<exchange_rates>
									<exchange_rate>
										<code>USD</code>
										<name>Dolar Estadounidense</name>
										<symbol>USD</symbol>
										<value>3812.76</value><!-- TRM financiera -->
									</exchange_rate>
									<exchange_rate>
										<code>EUR</code>
										<name>Euro</name>
										<symbol>$$$</symbol>
										<value>4521.93</value>
									</exchange_rate>
								</exchange_rates>
								<fare_data>
									<fare>
										<product_type>20</product_type>
										<fare_type>2</fare_type>
										<operator>
											<code>1</code>
											<name>Aviatur.travel</name>
										</operator>
										<provider>
											<code>999</code>
											<name>Hopper</name>
										</provider>
										<base_amount>131123</base_amount>
										<total_amount>131123</total_amount>
										<administrative_amount>0</administrative_amount>
										<administrative_amount_base>0</administrative_amount_base>
										<administrative_amount_tax>0</administrative_amount_tax>
										<commission_amount>0</commission_amount>
										<markup_type>1</markup_type> <!-- comision -->
										<markup_amount>0</markup_amount>
										<utility_amount>0</utility_amount>
										<taxes></taxes>
										<service_fares/>
										<optional_fares/>
										<!-- grats es para propinas de cruceros  -->
										<grats_info>
											<include>N</include><!--N no incluye -->
											<amount>0.00</amount>
										</grats_info>
									</fare>
								</fare_data>
								<cost_data>
									<fare>
										<product_type>20</product_type>
										<fare_type>2</fare_type>
										<operator>
											<code>1</code>
											<name>Aviatur.travel</name>
										</operator>
										<provider>
											<code>999</code>
											<name>Hopper</name>
										</provider>
										<base_amount>131123</base_amount>
										<total_amount>131123</total_amount>
										<administrative_amount>0</administrative_amount>
										<administrative_amount_base>0</administrative_amount_base>
										<administrative_amount_tax>0</administrative_amount_tax>
										<commission_amount>0</commission_amount>
										<markup_type>1</markup_type>
										<markup_amount>0</markup_amount>
										<utility_amount>0</utility_amount>
										<taxes></taxes>
										<service_fares/>
										<optional_fares/>
										<grats_info>
											<include>N</include>
											<amount>0.00</amount>
										</grats_info>
									</fare>
								</cost_data>
								<payment_currency>
									<code>COP</code>
									<name>Pesos Colombianos</name>
									<symbol>COP</symbol>
								</payment_currency>
								<travel_agency>
									<code>TAR</code>
									<name>Tiquetes Aviatur</name>
								</travel_agency>
								<language>
									<code>EN</code>
									<name>Espa&#xF1;ol</name>
								</language>
								<aerolinea>
									<code>{code}</code>
									<name>{name}</name>
								</aerolinea>
								<product_data/>
								<booking_data>
									<servicios>
										<servicio>
											<idservicio>12345678945</idservicio><!-- Reserva -->
											<tiposervicio>V</tiposervicio><!-- V = varos G= gastos fee-->
											<nombreservicio>GARANTIA DE TARIFAS HOPPER</nombreservicio>
											<descripcionservicio>GARANTIA DE TARIFAS HOPPER</descripcionservicio>
											<fechainicio>2021-10-10</fechainicio><!-- fecha donde se congelo -->
											<fechafin>2021-10-15</fechafin><!-- fecha maxima de regreso a la compra-->

											<idproveedor>95865</idproveedor><!--HOPPER INC proveedor -->
											<idprestador>34918</idprestador><!--HOPPER INC prestador-->

											<idproveedor/><!--crear el proveedor, preguntar a cristina para confirmar con ingrid-->
											<idprestador/><!-- igual a id prestador -->

											<claseservicio>N</claseservicio>
											<codigoservicionetoffice>VA</codigoservicionetoffice><!-- id de servicio hopper -->
											<codigomoneda>USD</codigomoneda><!-- por que se factura en COP pero expediente en USD -->
											<numeropasajeros>1</numeropasajeros>
											<ciudadorigen>BOG</ciudadorigen>
											<ciudaddestino>PEI</ciudaddestino>
											<items>
												<item>
													<codigomoneda>COP</codigomoneda><!-- debe ir USD-->
													<descripcion>GARANTIA DE TARIFAS HOPPER</descripcion>
													<unidad1>T</unidad1>
													<cantidad1>1</cantidad1>
													<unidad2>T</unidad2>
													<cantidad2>1</cantidad2>
													<tipotarifa>TP</tipotarifa><!-- TP = comisionable TN= tarifa neta-->
													<calculoutilidad>P</calculoutilidad>
													<tarifaproveedor>110188</tarifaproveedor>
													<totalproveedor>131123</totalproveedor>
													<!-- Quote es en USD -->
													<tarifaproveedor_quote>0</tarifaproveedor_quote><!-- valor de tarifa basado en TRM-->
													<totalproveedor_quote>0</totalproveedor_quote>
													<porcentajeutilidad>0.00</porcentajeutilidad>
													<valorutilidad>0.00</valorutilidad>
													<totalutilidad>0.00</totalutilidad>
													<!-- todos los tags de IVA deben ir en 0 -->
													<porcentajeiva>19.00</porcentajeiva>
													<valorivaproveedor>20936</valorivaproveedor>
													<totalivaproveedor>20936</totalivaproveedor>
													<valorivaventa>20936</valorivaventa>
													<totalotroscargos/>
													<totalventa>131123</totalventa><!-- tarifa neta-->
													<totalventa_quote>0</totalventa_quote><!-- tarifa neta en USD de TRM del día-->
													<otrosimpuestos><!-- por si otro producto tiene impuestos -->
														<impuesto>
															<codigo>1</codigo>
															<nombre>IVA</nombre>
															<basegravable>0</basegravable>
															<porcentaje>0</porcentaje>
															<valor>0</valor>
														</impuesto>
													</otrosimpuestos>
												</item>
											</items>
										</servicio>
									</servicios>
								</booking_data>
							</product>
						</data>
					</FILTRO>
				</ns:body>
			</ns:request>
		</ns:mbus>
	</soapenv:Body>
</soapenv:Envelope>

```
