# Solarwinds
Code vulnerability in the license verification library

<h2>Note</h2>
I do not condone piracy, and if you can afford to purchase a license for SolarWinds products, be sure to buy it!

<p align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/7/76/Official_SolarWinds_Logo.svg" alt="MAS Logo"></p>

<h3>Good day, dear friend!</h3>
<P>If you need software from Solarwinds but your company can't afford to buy a subscription for crazy money, I'm ready to help you solve this problem.</P>

<P>I worked for several weeks and achieved that the trial version was verified indefinitely, or more precisely until 9999, with full functionality and without restrictions on the number of nodes, ports, volumes.</P>

You can activate any product with my mod:
<ul>
<li>NPM - Network Performance Monitor</li>
<li>EOC - Enterprise Operations Console</li>
<li>IPAM - IP Address Manager</li>
<li>NCM - Network Configuration Management</li>
<li>NTA - NetFlow Traffic Analyzer</li>
<li>VoIP and Network Quality Manager</li>
<li>SCM - Server Configuration Monitor</li>
<li>SRM - Storage Resource Monitor</li>
<li>WPM - Web Performance Monitor</li>
<li>VM - Virtualization Manager</li>
<li>UDT - User Device Tracker</li>
<li>SAM - Server & Application Monitor</li>
<li>NAM - Network Automation Manager</li>
<li>LM - Log Management and Analysis</li>
<li>HA - High Availability</li>
<li>ACM - Application Centric Monitor</li>
</ul>

<h3>____________________ HCO _______________________</h3>
<ul>
<li>Observability Advanced Edition</li>
<li>Observability Advanced Enterprise Scale Edition</li>
<li>Observability Essentials Edition</li>
<li>Observability Essentials Enterprise Scale Edition</li>
</ul>

<h2>All products in the trial period are susceptible to this vulnerability.</h2>

<b>Vulnerability in the SolarWinds.Licensing.Gen4.Management namespace class</b>
<code>
		public DateTime Expiration
		{
			get
			{
				if (this._license.ExpirationDate != ExpirationDateType.Relative && this._license.OriginalAbsoluteExpirationDate == DateTime.MaxValue)
				{
					return this._license.AbsoluteExpirationDate;
				}
				DateTime dateTime = DateTime.Now.AllowTests();
				if (!(dateTime.AddHours(24.0) < this._license.InstantiationDate))
				{
					return this._license.AbsoluteExpirationDate;
				}
				return dateTime.AddMinutes(-1.0);
			}
		}
</code> 

<H3>A couple of screenshots</H3>
<hr>
After modification the day counter is set to maximum:

<p align="center"><img src="https://github.com/ShoutDown/Solarwinds/blob/main/scr-1.png"></p>

<p align="center"><img src="https://github.com/ShoutDown/Solarwinds/blob/main/scr-2.png"></p>

<b>And Network Topology Mapper also vulnerable</b>

<p align="center"><img src="https://github.com/ShoutDown/Solarwinds/blob/main/NTM.png"></p>

<b>And Engineer's Toolset</b>
<p align="center"><img src="https://raw.githubusercontent.com/ShoutDown/Solarwinds/refs/heads/main/Toolset.png"></p>

<H2>For more information, please contact our Telegram group.</H2>
If you need more detailed information, <a href="https://t.me/solarwinds_HCO"
   target="_blank"
   rel="noopener noreferrer"
   style="display:inline-flex;align-items:center;gap:8px;text-decoration:none;color:inherit;">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/82/Telegram_logo.svg/250px-Telegram_logo.svg.png"
       alt="Telegram"
       width="24"
       height="24"
       style="display:block;">
  <span>t.me/solarwinds_HCO</span>
</a>
