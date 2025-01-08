<article class="md-content__inner md-typeset">
                
                  



  <h1>Ticket Status</h1>

<h2 id="flight-ticket-statusdetails">Flight Ticket Status/Details</h2>
<div class="highlight"><pre><span></span><code tabindex="0">Endpoint: ~/ticket-details
Method: Post
Header Params: Content-Type  : application/json
Authorization : Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC9nZHMtYWRtaW4udGVzdFwvYXBpXC9pbnRsXC9hbmRyb2lkXC9pbml0aWFsaXplIiwiaWF0IjoxNjEzMzg1ODY3LCJleHAiOjE2MTMzODk0NjcsIm5iZiI6MTYxMzM4NTg2NywianRpIjoiY3o2eFZLdEVkd05jTTRVcCIsInN1YiI6MTMsInBydiI6IjQyZWRlMzMzNGEwNGNkNjVjYjJiZTNmNWFkZmViMmMxZWRkMzA3NzQifQ.UzEWszpOW92jOqSkdciWoGV4456CdS1nuPx7Tql-_Xk
</code></pre></div>
<p><code>Request Body</code></p>
<div class="md-typeset__scrollwrap"><div class="md-typeset__table"><table>
<thead>
<tr>
<th>ATTRIBUTE</th>
<th>DATATYPE</th>
<th>RQUIRED</th>
<th>VALUES</th>
</tr>
</thead>
<tbody>
<tr>
<td>bookingReferenceID</td>
<td>bookingReferenceID from booking response</td>
<td>required</td>
<td></td>
</tr>
<tr>
<td>tripType</td>
<td>string</td>
<td>required</td>
<td>Trip Type</td>
</tr>
<tr>
<td>PNR</td>
<td>string</td>
<td>optional</td>
<td>PNR</td>
</tr>
</tbody>
</table></div></div>
<p><code>Sample Request</code></p>
<div class="highlight"><pre><span></span><code><span class="w">    </span><span class="p">{</span>
<span class="w">        </span><span class="nt">"bookingReferenceID"</span><span class="p">:</span><span class="w"> </span><span class="s2">"e1caec16-f675-48ea-a40c-5e1d05741300"</span><span class="p">,</span>
<span class="w">        </span><span class="nt">"tripType"</span><span class="p">:</span><span class="w"> </span><span class="s2">"oneway"</span><span class="p">,</span>
<span class="w">        </span><span class="nt">"PNR"</span><span class="p">:</span><span class="w"> </span><span class="s2">"PQMJ8E"</span>
<span class="w">    </span><span class="p">}</span>
</code></pre></div>
<p><code>Sample Response</code></p>
<div class="tabbed-set tabbed-alternate" data-tabs="1:3" style="--md-indicator-x: 0px; --md-indicator-width: 82px;"><input checked="checked" id="__tabbed_1_1" name="__tabbed_1" type="radio"><input id="__tabbed_1_2" name="__tabbed_1" type="radio"><input id="__tabbed_1_3" name="__tabbed_1" type="radio"><div class="tabbed-labels"><label for="__tabbed_1_1">One Way</label><label for="__tabbed_1_2">Round Trip</label><label for="__tabbed_1_3">Multi City</label></div>
<div class="tabbed-content">
<div class="tabbed-block">
<div class="highlight"><pre><span></span><code tabindex="0"><span class="p">{</span>
<span class="w">    </span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="kc">true</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"data"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">        </span><span class="nt">"ticketSummary"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"ticketReferenceID"</span><span class="p">:</span><span class="w"> </span><span class="s2">"29f27b24-3f33-4190-9835-9859c790fc47"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"PNR"</span><span class="p">:</span><span class="w"> </span><span class="s2">"PQMJ8E"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"tripType"</span><span class="p">:</span><span class="w"> </span><span class="s2">"oneway"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"currency"</span><span class="p">:</span><span class="w"> </span><span class="s2">"NPR"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"issued_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tue, Feb 14, 2023"</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"flightSummary"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"airline_confirmation_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"PQMJ8E"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-07-22"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"10:10 AM"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-07-22"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"12:25 PM"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"05 Hr 00 Min"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"depart_city_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"KTM"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"depart_city_airport_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tribhuvan Intl Airport"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"depart_city_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Kathmandu City"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"depart_city_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Nepal"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"carrierCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"QR"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"carrierLogo"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1633428326-1898803185.png"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"carrierName"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Qatar Airways"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"dest_city_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DOH"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"dest_city_airport_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Hamad Int’l Airport"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"dest_city_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Doha"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"dest_city_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Qatar"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"flight_segments"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span>
<span class="w">                </span><span class="p">{</span>
<span class="w">                    </span><span class="nt">"carrierCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"QR"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierName"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Qatar Airways"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierLogo"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1633428326-1898803185.png"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"flight_number"</span><span class="p">:</span><span class="w"> </span><span class="s2">"653"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"flight_equipment"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Airbus A330-300"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"cabin_class"</span><span class="p">:</span><span class="w"> </span><span class="s2">"M"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-07-22"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"10:10 AM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-07-22"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"12:25 PM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"05:00:00"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"KTM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tribhuvan Intl Airport"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Kathmandu City"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Nepal"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">"I"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DOH"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Hamad Int’l Airport"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Doha"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Qatar"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_connection_time"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span>
<span class="w">                </span><span class="p">}</span>
<span class="w">            </span><span class="p">]</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"fareInformation"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"total_adt"</span><span class="p">:</span><span class="w"> </span><span class="mi">41893</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"total_chd"</span><span class="p">:</span><span class="w"> </span><span class="mi">0</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"total_inf"</span><span class="p">:</span><span class="w"> </span><span class="mi">0</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"total_cost"</span><span class="p">:</span><span class="w"> </span><span class="mi">41893</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"cashBack"</span><span class="p">:</span><span class="w"> </span><span class="mi">300</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"baggageDetails"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"cabin"</span><span class="p">:</span><span class="w"> </span><span class="s2">"7 Kg"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"baggage"</span><span class="p">:</span><span class="w"> </span><span class="s2">"30 Kg"</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"passengers"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span>
<span class="w">            </span><span class="p">{</span>
<span class="w">                </span><span class="nt">"passenger_type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"ADT"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"passenger_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Maharjan Rabi"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"eticket_number"</span><span class="p">:</span><span class="w"> </span><span class="s2">"157-6752209683"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"PNR"</span><span class="p">:</span><span class="w"> </span><span class="s2">"PQMJ8E"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"airlines_confirmation"</span><span class="p">:</span><span class="w"> </span><span class="s2">"PQMJ8E"</span>
<span class="w">            </span><span class="p">}</span>
<span class="w">        </span><span class="p">],</span>
<span class="w">        </span><span class="nt">"contactDetails"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"email"</span><span class="p">:</span><span class="w"> </span><span class="s2">"maharjanrabi1@gmail.com"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"phone"</span><span class="p">:</span><span class="w"> </span><span class="s2">"9849932310"</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"eticketLink"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights-private.s3.ap-southeast-1.amazonaws.com/tickets/PQMJ8E-1676354461.pdf?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIA4CEOEY6AUXGMCTXF%2F20230214%2Fap-southeast-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230214T060104Z&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Expires=900&amp;X-Amz-Signature=a834632054848ad610561f9a7588a1ff789ae2a35c7991f091d97a043ed7d043"</span>
<span class="w">    </span><span class="p">}</span>
<span class="p">}</span>
</code></pre></div>
</div>
<div class="tabbed-block">
<div class="highlight"><pre><span></span><code><span class="p">{</span>
<span class="w">    </span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="kc">true</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"data"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">        </span><span class="nt">"ticketSummary"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"ticketReferenceID"</span><span class="p">:</span><span class="w"> </span><span class="s2">"f767edef-1334-4ac9-ae02-2f328db9fd8c"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"PNR"</span><span class="p">:</span><span class="w"> </span><span class="s2">"PQVBOE"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"tripType"</span><span class="p">:</span><span class="w"> </span><span class="s2">"round"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"currency"</span><span class="p">:</span><span class="w"> </span><span class="s2">"NPR"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"issued_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tue, Feb 14, 2023"</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"flightSummary"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"airline_confirmation_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"PQVBOE"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-07-22"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"10:10 AM"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"depart_city_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"KTM"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"depart_city_airport_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tribhuvan Intl Airport"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"depart_city_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Kathmandu City"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"depart_city_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Nepal"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-07-22"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"12:25 PM"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"05 Hr 00 Min"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"dest_city_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DOH"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"dest_city_airport_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Hamad Int’l Airport"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"dest_city_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Doha"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"dest_city_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Qatar"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"carrierCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"QR"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"carrierLogo"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1633428326-1898803185.png"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"carrierName"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Qatar Airways"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-07-30"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"00:35 AM"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_depart_city_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DOH"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_depart_city_airport_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Hamad Int’l Airport"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_depart_city_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Doha"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_depart_city_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Qatar"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-07-30"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"08:05 AM"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"04 Hr 45 Min"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_dest_city_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"KTM"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_dest_city_airport_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tribhuvan Intl Airport"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_dest_city_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Kathmandu City"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"return_dest_city_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Nepal"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"carrierCodeReturn"</span><span class="p">:</span><span class="w"> </span><span class="s2">"QR"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"carrierLogoReturn"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1633428326-1898803185.png"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"carrierNameReturn"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Qatar Airways"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"flight_segments_outbound"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span>
<span class="w">                </span><span class="p">{</span>
<span class="w">                    </span><span class="nt">"carrierCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"QR"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierName"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Qatar Airways"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierLogo"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1633428326-1898803185.png"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"flight_number"</span><span class="p">:</span><span class="w"> </span><span class="s2">"653"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"flight_equipment"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Airbus A330-300"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"cabin_class"</span><span class="p">:</span><span class="w"> </span><span class="s2">"M"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-07-22"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"10:10 AM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-07-22"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"12:25 PM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"05:00:00"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"KTM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tribhuvan Intl Airport"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Kathmandu City"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Nepal"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">"I"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DOH"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Hamad Int’l Airport"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Doha"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Qatar"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_connection_time"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span>
<span class="w">                </span><span class="p">}</span>
<span class="w">            </span><span class="p">],</span>
<span class="w">            </span><span class="nt">"flight_segments_return"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span>
<span class="w">                </span><span class="p">{</span>
<span class="w">                    </span><span class="nt">"carrierCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"QR"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierName"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Qatar Airways"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierLogo"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/1633428326-1898803185.png"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"flight_number"</span><span class="p">:</span><span class="w"> </span><span class="s2">"652"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"flight_equipment"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Airbus A330-300"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"cabin_class"</span><span class="p">:</span><span class="w"> </span><span class="s2">"M"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-07-30"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"00:35 AM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-07-30"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"08:05 AM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"04:45:00"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DOH"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Hamad Int’l Airport"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Doha"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Qatar"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">""</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"KTM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tribhuvan Intl Airport"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Kathmandu City"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Nepal"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">"I"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_connection_time"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span>
<span class="w">                </span><span class="p">}</span>
<span class="w">            </span><span class="p">]</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"fareInformation"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"total_adt"</span><span class="p">:</span><span class="w"> </span><span class="mi">41893</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"total_chd"</span><span class="p">:</span><span class="w"> </span><span class="mi">0</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"total_inf"</span><span class="p">:</span><span class="w"> </span><span class="mi">0</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"total_cost"</span><span class="p">:</span><span class="w"> </span><span class="mi">41893</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"cashBack"</span><span class="p">:</span><span class="w"> </span><span class="mi">300</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"baggageDetails"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"outbound"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">                </span><span class="nt">"cabin"</span><span class="p">:</span><span class="w"> </span><span class="s2">"7 Kg"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"baggage"</span><span class="p">:</span><span class="w"> </span><span class="s2">"30 Kg"</span>
<span class="w">            </span><span class="p">},</span>
<span class="w">            </span><span class="nt">"return"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">                </span><span class="nt">"cabin"</span><span class="p">:</span><span class="w"> </span><span class="s2">"7 Kg"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"baggage"</span><span class="p">:</span><span class="w"> </span><span class="s2">"25 Kg"</span>
<span class="w">            </span><span class="p">}</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"passengers"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span>
<span class="w">            </span><span class="p">{</span>
<span class="w">                </span><span class="nt">"passenger_type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"ADT"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"passenger_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Maharjan Rabi"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"eticket_number"</span><span class="p">:</span><span class="w"> </span><span class="s2">"157-6752209684"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"PNR"</span><span class="p">:</span><span class="w"> </span><span class="s2">"PQVBOE"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"airlines_confirmation"</span><span class="p">:</span><span class="w"> </span><span class="s2">"PQVBOE"</span>
<span class="w">            </span><span class="p">}</span>
<span class="w">        </span><span class="p">],</span>
<span class="w">        </span><span class="nt">"contactDetails"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"email"</span><span class="p">:</span><span class="w"> </span><span class="s2">"maharjanrabi1@gmail.com"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"phone"</span><span class="p">:</span><span class="w"> </span><span class="s2">"9849932310"</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"eticketLink"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights-private.s3.ap-southeast-1.amazonaws.com/tickets/PQMJ8E-1676354461.pdf?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIA4CEOEY6AUXGMCTXF%2F20230214%2Fap-southeast-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230214T060104Z&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Expires=900&amp;X-Amz-Signature=a834632054848ad610561f9a7588a1ff789ae2a35c7991f091d97a043ed7d043"</span>
<span class="w">    </span><span class="p">}</span>
<span class="p">}</span>
</code></pre></div>
</div>
<div class="tabbed-block">
<div class="highlight"><pre><span></span><code><span class="p">{</span>
<span class="w">    </span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="kc">true</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"data"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">        </span><span class="nt">"ticketSummary"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"ticketReferenceID"</span><span class="p">:</span><span class="w"> </span><span class="s2">"c6493116-25b8-4105-a26a-1c79937c5421"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"PNR"</span><span class="p">:</span><span class="w"> </span><span class="s2">"PQXM2B"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"tripType"</span><span class="p">:</span><span class="w"> </span><span class="s2">"multicity"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"currency"</span><span class="p">:</span><span class="w"> </span><span class="s2">"NPR"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"issued_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tue, Feb 14, 2023"</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"flightSummary"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"flight_segments"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span>
<span class="w">                </span><span class="p">{</span>
<span class="w">                    </span><span class="nt">"airline_confirmation_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"197IJB"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-01"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"15:45 PM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-02"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"03:20 AM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"01 Hr 45 Min"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"KTM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tribhuvan Intl Airport"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Kathmandu City"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Nepal"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DEL"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Indira Gandhi Int’l Airport"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"New Delhi"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"India"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"FZ"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierLogo"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierName"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Fly Dubai"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"connecting_segments"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span>
<span class="w">                        </span><span class="p">{</span>
<span class="w">                            </span><span class="nt">"carrierCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"FZ"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"carrierName"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Fly Dubai"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"carrierLogo"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"flight_number"</span><span class="p">:</span><span class="w"> </span><span class="s2">"540"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"flight_equipment"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Boeing 737"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"cabin_class"</span><span class="p">:</span><span class="w"> </span><span class="s2">"M"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-01"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"15:45 PM"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-01"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"18:50 PM"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"04:50:00"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"KTM"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tribhuvan Intl Airport"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Kathmandu City"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Nepal"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">"I"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DXB"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Dubai Int’l Airport"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Dubai"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"United Arab Emirates"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_connection_time"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span>
<span class="w">                        </span><span class="p">},</span>
<span class="w">                        </span><span class="p">{</span>
<span class="w">                            </span><span class="nt">"carrierCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"FZ"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"carrierName"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Fly Dubai"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"carrierLogo"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"flight_number"</span><span class="p">:</span><span class="w"> </span><span class="s2">"431"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"flight_equipment"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Boeing 737"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"cabin_class"</span><span class="p">:</span><span class="w"> </span><span class="s2">"M"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-01"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"22:10 PM"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-02"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"03:20 AM"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"03:40:00"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DXB"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Dubai Int’l Airport"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Dubai"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"United Arab Emirates"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DEL"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Indira Gandhi Int’l Airport"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"New Delhi"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"India"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">"3"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_connection_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"05 hr 10 min"</span>
<span class="w">                        </span><span class="p">}</span>
<span class="w">                    </span><span class="p">]</span>
<span class="w">                </span><span class="p">},</span>
<span class="w">                </span><span class="p">{</span>
<span class="w">                    </span><span class="nt">"airline_confirmation_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"197IJB"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-10"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"04:20 AM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-10"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"07:00 AM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"01 Hr 45 Min"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DEL"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Indira Gandhi Int’l Airport"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"New Delhi"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"India"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DXB"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Dubai Int’l Airport"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Dubai"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"United Arab Emirates"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"FZ"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierLogo"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierName"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Fly Dubai"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"connecting_segments"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span>
<span class="w">                        </span><span class="p">{</span>
<span class="w">                            </span><span class="nt">"carrierCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"FZ"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"carrierName"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Fly Dubai"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"carrierLogo"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"flight_number"</span><span class="p">:</span><span class="w"> </span><span class="s2">"432"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"flight_equipment"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Boeing 737"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"cabin_class"</span><span class="p">:</span><span class="w"> </span><span class="s2">"M"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-10"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"04:20 AM"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-10"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"07:00 AM"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"04:10:00"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DEL"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Indira Gandhi Int’l Airport"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"New Delhi"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"India"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">"3"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DXB"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Dubai Int’l Airport"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Dubai"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"United Arab Emirates"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_connection_time"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span>
<span class="w">                        </span><span class="p">}</span>
<span class="w">                    </span><span class="p">]</span>
<span class="w">                </span><span class="p">},</span>
<span class="w">                </span><span class="p">{</span>
<span class="w">                    </span><span class="nt">"airline_confirmation_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"197IJB"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-15"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"13:50 PM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-15"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"20:00 PM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"01 Hr 45 Min"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DXB"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Dubai Int’l Airport"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Dubai"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_departure_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"United Arab Emirates"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"KTM"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tribhuvan Intl Airport"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Kathmandu City"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"seg_arrival_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Nepal"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"FZ"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierLogo"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"carrierName"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Fly Dubai"</span><span class="p">,</span>
<span class="w">                    </span><span class="nt">"connecting_segments"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span>
<span class="w">                        </span><span class="p">{</span>
<span class="w">                            </span><span class="nt">"carrierCode"</span><span class="p">:</span><span class="w"> </span><span class="s2">"FZ"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"carrierName"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Fly Dubai"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"carrierLogo"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights.s3.ap-southeast-1.amazonaws.com/airlines/FZ_flydubai.png"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"flight_number"</span><span class="p">:</span><span class="w"> </span><span class="s2">"573"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"flight_equipment"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Boeing 737"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"cabin_class"</span><span class="p">:</span><span class="w"> </span><span class="s2">"M"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-15"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"13:50 PM"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_date"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2023-08-15"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_time"</span><span class="p">:</span><span class="w"> </span><span class="s2">"20:00 PM"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_total_flying_hours"</span><span class="p">:</span><span class="w"> </span><span class="s2">"04:25:00"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"DXB"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Dubai Int’l Airport"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Dubai"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"United Arab Emirates"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_departure_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">"2"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_airport_code"</span><span class="p">:</span><span class="w"> </span><span class="s2">"KTM"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_airport"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Tribhuvan Intl Airport"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_city"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Kathmandu City"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_country"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Nepal"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_arrival_terminal"</span><span class="p">:</span><span class="w"> </span><span class="s2">"I"</span><span class="p">,</span>
<span class="w">                            </span><span class="nt">"seg_connection_time"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span>
<span class="w">                        </span><span class="p">}</span>
<span class="w">                    </span><span class="p">]</span>
<span class="w">                </span><span class="p">}</span>
<span class="w">            </span><span class="p">]</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"fareInformation"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"total_adt"</span><span class="p">:</span><span class="w"> </span><span class="mi">41893</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"total_chd"</span><span class="p">:</span><span class="w"> </span><span class="mi">0</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"total_inf"</span><span class="p">:</span><span class="w"> </span><span class="mi">0</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"total_cost"</span><span class="p">:</span><span class="w"> </span><span class="mi">41893</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"cashBack"</span><span class="p">:</span><span class="w"> </span><span class="mi">300</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"baggageDetails"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"cabin"</span><span class="p">:</span><span class="w"> </span><span class="s2">"7 Kg"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"baggage"</span><span class="p">:</span><span class="w"> </span><span class="s2">"20 Kg"</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"passengers"</span><span class="p">:</span><span class="w"> </span><span class="p">[</span>
<span class="w">            </span><span class="p">{</span>
<span class="w">                </span><span class="nt">"passenger_type"</span><span class="p">:</span><span class="w"> </span><span class="s2">"ADT"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"passenger_name"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Maharjan Rabi"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"eticket_number"</span><span class="p">:</span><span class="w"> </span><span class="s2">"141-6752209685"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"PNR"</span><span class="p">:</span><span class="w"> </span><span class="s2">"PQXM2B"</span><span class="p">,</span>
<span class="w">                </span><span class="nt">"airlines_confirmation"</span><span class="p">:</span><span class="w"> </span><span class="s2">"197IJB"</span>
<span class="w">            </span><span class="p">}</span>
<span class="w">        </span><span class="p">],</span>
<span class="w">        </span><span class="nt">"contactDetails"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">            </span><span class="nt">"email"</span><span class="p">:</span><span class="w"> </span><span class="s2">"maharjanrabi1@gmail.com"</span><span class="p">,</span>
<span class="w">            </span><span class="nt">"phone"</span><span class="p">:</span><span class="w"> </span><span class="s2">"9849932310"</span>
<span class="w">        </span><span class="p">},</span>
<span class="w">        </span><span class="nt">"eticketLink"</span><span class="p">:</span><span class="w"> </span><span class="s2">"https://sastotickets-flights-private.s3.ap-southeast-1.amazonaws.com/tickets/PQMJ8E-1676354461.pdf?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&amp;X-Amz-Algorithm=AWS4-HMAC-SHA256&amp;X-Amz-Credential=AKIA4CEOEY6AUXGMCTXF%2F20230214%2Fap-southeast-1%2Fs3%2Faws4_request&amp;X-Amz-Date=20230214T060104Z&amp;X-Amz-SignedHeaders=host&amp;X-Amz-Expires=900&amp;X-Amz-Signature=a834632054848ad610561f9a7588a1ff789ae2a35c7991f091d97a043ed7d043"</span>
<span class="w">    </span><span class="p">}</span>
<span class="p">}</span>
</code></pre></div>
</div>
</div>
<div class="tabbed-control tabbed-control--prev" hidden=""><button class="tabbed-button" tabindex="-1" aria-hidden="true"></button></div><div class="tabbed-control tabbed-control--next" hidden=""><button class="tabbed-button" tabindex="-1" aria-hidden="true"></button></div></div>
<p><br></p>
<p><code>Sample Error Response</code></p>
<div class="highlight"><pre><span></span><code><span class="err">Case</span><span class="p">:</span><span class="w"> </span><span class="err">Valida</span><span class="kc">t</span><span class="err">io</span><span class="kc">n</span><span class="w"> </span><span class="err">Error</span>
<span class="p">{</span>
<span class="w">    </span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"data"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">        </span><span class="nt">"error"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Invalid Ticket Parameters."</span>
<span class="w">    </span><span class="p">}</span>
<span class="p">}</span>

<span class="err">Case</span><span class="p">:</span><span class="w"> </span><span class="err">Booki</span><span class="kc">n</span><span class="err">g</span><span class="w"> </span><span class="kc">transa</span><span class="err">c</span><span class="kc">t</span><span class="err">io</span><span class="kc">n</span><span class="w"> </span><span class="kc">n</span><span class="err">o</span><span class="kc">t</span><span class="w"> </span><span class="kc">f</span><span class="err">ou</span><span class="kc">n</span><span class="err">d</span>
<span class="p">{</span>
<span class="w">    </span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"data"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">        </span><span class="nt">"error"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Booking Records Not Found."</span>
<span class="w">    </span><span class="p">}</span>
<span class="p">}</span>


<span class="err">Case</span><span class="p">:</span><span class="w"> </span><span class="err">Ticke</span><span class="kc">t</span><span class="err">i</span><span class="kc">n</span><span class="err">g</span><span class="w"> </span><span class="err">Failed</span><span class="w"> </span><span class="err">or</span><span class="w"> </span><span class="err">No</span><span class="kc">t</span><span class="w"> </span><span class="err">Fou</span><span class="kc">n</span><span class="err">d</span>
<span class="p">{</span>
<span class="w">    </span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"data"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">        </span><span class="nt">"error"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Ticket Records Not Found. Ticket issue failed."</span>
<span class="w">    </span><span class="p">}</span>
<span class="p">}</span>

<span class="p">{</span>
<span class="w">    </span><span class="nt">"success"</span><span class="p">:</span><span class="w"> </span><span class="kc">false</span><span class="p">,</span>
<span class="w">    </span><span class="nt">"data"</span><span class="p">:</span><span class="w"> </span><span class="p">{</span>
<span class="w">        </span><span class="nt">"error"</span><span class="p">:</span><span class="w"> </span><span class="s2">"Ticket issue failed. Please contact customer support for more details."</span>
<span class="w">    </span><span class="p">}</span>
<span class="p">}</span>
</code></pre></div>





                
              </article>