# GSA Cisco AnyConnect

Copy the below text to /opt/cisco/anyconnect/profile/gsa_cp-gfeotp.xml


<?xml version="1.0" encoding="UTF-8"?>
<AnyConnectProfile xmlns="http://schemas.xmlsoap.org/encoding/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://schemas.xmlsoap.org/encoding/ AnyConnectProfile.xsd">
	<ClientInitialization>
		<UseStartBeforeLogon UserControllable="true">true</UseStartBeforeLogon>
		<AutomaticCertSelection UserControllable="true">true</AutomaticCertSelection>
		<ShowPreConnectMessage>false</ShowPreConnectMessage>
		<CertificateStore>All</CertificateStore>
		<CertificateStoreOverride>true</CertificateStoreOverride>
		<ProxySettings>IgnoreProxy</ProxySettings>
		<AllowLocalProxyConnections>true</AllowLocalProxyConnections>
		<AuthenticationTimeout>12</AuthenticationTimeout>
		<AutoConnectOnStart UserControllable="true">false</AutoConnectOnStart>
		<MinimizeOnConnect UserControllable="true">true</MinimizeOnConnect>
		<LocalLanAccess UserControllable="true">true</LocalLanAccess>
		<DisableCaptivePortalDetection UserControllable="true">false</DisableCaptivePortalDetection>
		<ClearSmartcardPin UserControllable="false">false</ClearSmartcardPin>
		<IPProtocolSupport>IPv4,IPv6</IPProtocolSupport>
		<AutoReconnect UserControllable="false">true
			<AutoReconnectBehavior UserControllable="false">DisconnectOnSuspend</AutoReconnectBehavior>
		</AutoReconnect>
		<AutoUpdate UserControllable="false">true</AutoUpdate>
		<RSASecurIDIntegration UserControllable="false">Automatic</RSASecurIDIntegration>
		<WindowsLogonEnforcement>SingleLocalLogon</WindowsLogonEnforcement>
		<WindowsVPNEstablishment>LocalUsersOnly</WindowsVPNEstablishment>
		<AutomaticVPNPolicy>false</AutomaticVPNPolicy>
		<PPPExclusion UserControllable="false">Disable
			<PPPExclusionServerIP UserControllable="false"></PPPExclusionServerIP>
		</PPPExclusion>
		<EnableScripting UserControllable="false">true
			<TerminateScriptOnNextEvent>false</TerminateScriptOnNextEvent>
			<EnablePostSBLOnConnectScript>true</EnablePostSBLOnConnectScript>
		</EnableScripting>
		<CertificateMatch>
			<MatchOnlyCertsWithKU>false</MatchOnlyCertsWithKU>
			<KeyUsage>
				<MatchKey>Digital_Signature</MatchKey>
			</KeyUsage>
			<ExtendedKeyUsage>
				<ExtendedMatchKey>ClientAuth</ExtendedMatchKey>
			</ExtendedKeyUsage>
		</CertificateMatch>
		<EnableAutomaticServerSelection UserControllable="true">true
			<AutoServerSelectionImprovement>20</AutoServerSelectionImprovement>
			<AutoServerSelectionSuspendTime>4</AutoServerSelectionSuspendTime>
		</EnableAutomaticServerSelection>
		<RetainVpnOnLogoff>false
		</RetainVpnOnLogoff>
		<AllowManualHostInput>true</AllowManualHostInput>
	</ClientInitialization>
	<ServerList>
		<HostEntry>
			<HostName>GSA Access OTP</HostName>
			<HostAddress>vpn.gsa.gov</HostAddress>
			<UserGroup>gfeotp</UserGroup>
		</HostEntry>
	</ServerList>
</AnyConnectProfile>
