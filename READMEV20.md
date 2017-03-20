

**JSON File management for Lifeguard asset monitoring**

## Version History
 
20. monitoring_configuration_V20
    ```
    Date 20/03/2017  
- Readme Changes
  - Revisions re-ordered from most recent
  - Change items ordered to match Version
  - Version now monitoring_configuration (not Wanda)
 
- All	
  - Removed agreeded items
  - Edited frequencies
  - Added Firmware for all units
  - Some SMS naming conventions harmonised

- BARCO 	
  - Split out to Series 1 and Series 2

- Doremi
  - Doremi ShowVault	Identical as Doremi but with all exisiting media_block itmes (7 in total)
  - Doremi IMB units	added capitals to the sda/sdb/sdc items becoming SDA/SDB/SDC
  - removed playback channel working state
  - MD0 idetified as Global content and renamed RAID_data_usage/RAID_data_state and RAID_data_working_state
  - MD1 state/usage and working state removed
 
- Doremi DCP2000
  - Corrected Spelling errors (volatage to voltage)
  - Added hardware_SM_software_version
  - Removed warning threshold on software_integrity_check as known bugs causing lots of LG warnings
  - removed Voltage Working states to reduce items
  - removed RTC Battery as not availabe on DCP2000
  - removed playback channel working state
  - changed system model to hardware_model

- Christie IMB
  - IMB-S2	Renamed SM version to match Doremi system_security_manager_version
  - IMB-S2	Removed playback duration and timecode
  - IMB-S2 and E3LH	Renamed Priamry NAS to RAID Data capacity to match Doremi units
  - IMB-S2 and E3LH	Also Free disk space to RAID_data_free_disck_size 
  - IMB-S2 and E3LH	Made both IMB-S2 and E3LH primary drive available to  RAID_primary_drive_avaialable
  - IMB-S2 and E3LH	changed from system_SM_serial_number to system_serial_number
  - IMB-S2 added RAID_status

- Dolby
  - Added RAID_showstore_disk_capacity
  - Removed RAID_showstore_storage_status_array (stops verifying alerts shown as Degraded

19. Wanda_json_100_v19
    ```
    Date 09/03/2017
- Christie E3LH added

- Christie CP2000-X added

- Christie CP2000-XB added

- Christie CP42lH
  - Added Douser Status
  - Added Lens Prime Lens Type
  - Added Hardware LD Version

 -Christie CP4230, CP4220, CP2230, CP2220, CP2215, CP2210
  - Removed Lamp Error State
  - Added Lamp Status
  - Added Douser Status
  - Added System Power Status
  - Added Hardware LD Version

- Christie Solaria One, Solaria One+, CP2208, CP2208LP
  - Removed Lamp Error State
  - Added Lamp Status
  - Added Douser Status
  - Added System Power Status

- Christie CP2000-SB, CP2000-S, CP2000, CP2000-XB, CP2000-X
  - OID changed for System Power Status
  - Transform Type changed for Lamp LiteLOC Status (from CDS_lamp_Status_liteLOC to liteLOC_Status)
  - Lamp Output renamed to Light FL Output
  - Added unit (fL) to Light FL Output
  - Added Lamp Total Hours ON
  - Added Diagnostics SSM Self Test Fail
  - Added Diagnostics Power Up Self Test Fail
  - Added Diagnostics Ballast Com Fail
  - System Total Hours renamed to System Projector Hours

- Christie CP2000-ZX
  - OID changed for System Power Status
  - Added Douser Status
  - System Total Hours renamed to System Projector Hours

- Christie CP2000-M
  - Fixed typo on Fans Light Engine Fail
  - OID changed for System Power Status
  - Added Douser Status
  - System Total Hours renamed to System Projector Hours
  - Temperature Lamp Exhaust Limit renamed to Temperature Exhaust Air Limit
  - Temperature Light Exhaust renamed to Temperature Exhaust Air

- Barco ICMP
  - Hardware Serial Number renamed to System Serial Number

- Barco Projectors
  - Fixed typo on Diagnostics Proj Errors Count
  - Added Lamp Current Serial Number
  - Added System Projector Hours
  - Removed Lamp Total Strikes

- NEC Series 1 Projectors
  - System Active Input Port renamed to System Current Selected Input
  - System Active Title Name renamed to System Active Preset
  - Removed System Active Title Number
  - Removed System Active Data
  - Removed System Subtitle Status
  - Diagnostics Error Count renamed to Diagnostics Proj Errors Count
  - Temperature Cinema Board Ambient renamed to Temperature Cinema Board
  - Temperature Cinema Board Chest renamed to Temperature Card Cage
  - Temperature Inside Air renamed to Temperature Internal Board
  - OID changed for Software Version (see next)
  - Firmware Version renamed to Software Version
  - System Cinema Board Version renamed to System TI Version
  - System Power On Time renamed to System Total Hours

- NEC Series 2 Projectors
  - System Active Input Port renamed to System Current Selected Input
  - System Active Title Name renamed to System Active Preset
  - Removed System Active Title Number
  - Removed System Active Data
  - Removed System Active 3D
  - Temperature Exhaust renamed to Temperature Exhaust Air
  - OID changed for Software Version (see next)
  - System NEC Main Version renamed to Software Version
  - Removed Firmware Version
  - System ICP Version renamed to Hardware ICP Software Version
  - System SIB Version renamed to Hardware SIB Version
  - System LD Version renamed to Hardware LD Version
  - Removed System MMS Version
  - Diagnostics Marriage Fail renamed to Security Marriage State
  - Diagnostics Lamphouse Over Time renamed to Lamp Lamphouse Over Time
  - Diagnostics Self Test Error renamed to Diagnostics Power Up Self Test Fail
  - Security Enclosure Not Armed renamed to Security Enclosure Armed

18. Wanda_json_100_v18
    ```
    Date 23/02/2017
- CP42LH	
  - Removed GW/MAC/SNMP1 and 2
 
- All S2 Christie 	
  - Added IP address (Speeds up support)

- All S2 Christie	
  - Added Projector Hours

- All S2 Christie	
  - Added SMPTE Errors
 
- CP2208-LP	
 - Removed some lamp items, added LaPh Wheel Speed (NEED TO TEST AGAINST A CP2208-LP –Will aim to go to Christie to do this)
 
- CP2208/Sol1	
 - Removed SMPTE 292 errors (it does not have HD-SDI inputs)
 
- Christie S2-IMB	
 - Corrected ICP Comms critical State to correct threshold value
 
- CP200SB	
  - Removed Prime lens Status
  - Removed TI IB and CPU board serial numbers
  - Removed previous lamp data (Type and hours)
  - Added Lamp Voltage
  - Removed i2C item (N/A)
  - Added Proj resolution to match S2 models
  
- CP2000ZX
  - Removed EDID Checksum to reduce diagnostic count
  - Removed previous lamp data (Type and hours)
  - Removed Prime lens Status
  - Removed TI IB and CPU board serial numbers
  - Correct Temperature and Fan monitoring fields
  - Added Speed (RPM) over 'too slow' warning. Still keeping Fail
  - Corrected i2c Temperatures
  - Added Proj resolution to match S2 models
  
- CP2000M	
  -Corrected fans, temperature and interlock information which was inherited from the original LG file
  - Added Speed (RPM) over 'too slow' warning. Still keeping Fail
  - Removed Prime lens Status
  - Removed previous lamp data (Type and hours)
  - Added Proj resolution to match S2 models
  
- BARCO
  - Added Prime Lens Type
  - restored missing Diagnostic lists (top 4 faults, plus top 4 BARCO Error Codes)
  - Restored Maintenance Countdowns
  - Removed Lamp status as response is not displayed well by LG (0x01 only). Error list captures ALL faults.

17. Wanda_json_100_v17
    ```
    v17 21/02/2017
- Changed all Monitoring Types to Lower Case, excluding acronyms such as DMD, LPSU, etc...
- Some Monitoring types had spaces in them. They've been replaced with the standard underscore
- Some Monitoring types had two consecutive underscores, replace with a single one
- Fixed a couple of typing errors

16. Wanda_json_100_v16
    ```
    v16 07/02/2017
- Changed to Lower Case to match Database requirements for Remaining Lamp Life reporting:
  - lamp_hours
  - lamp_typelamp_life
  - lamp_life
  - lamp_hours_remaining

15. Wanda_json_100_v15
    ```
    v15 30/01/2017
- Added Christie confirmed Fibre Bundle and Diffuser temperature thresholds for Warning and critical on CP42LH

14. Wanda_json_100_v14
    ```
    v14 26/01/2017
- correct some temperature thresholds on CP42LH

13. Wanda_json_100_v13
    ```
    v13 25/01/2017
- CP2208 and Cp2208LP now separate 
- Diagnostics_LaserPhosphor_Power_Fault’ removed from all but the CP2208LP listing 
- CP42LH added

12. Wanda_json_100_v12
    ```
    v12 11/01/2017
- Add LMS to JSON to monitor lms-data Storage

11. Wanda_json_100_v11
    ```
    v11 06/01/2017
- Monitoring type name changed for NEC incorrect description (Lamp_Life > Lamp_Hours_Remaining)

  - {"name" : "Lamp_Life" , "oid" : "1.3.6.1.4.1.119.2.3.123.2.6.2.0", "freq": 600, "group" : "Lamp", "version" : 1} * removed
  - {"name" : "Lamp_Hours_Remaining" , "oid" : "1.3.6.1.4.1.119.2.3.123.2.6.2.0", "freq": 600, "group" : "Lamp", "version" : 1} ** added

10. Wanda_json_100_v10
    ```
    v10 04/01/2017
- Dolby software version oid changed from 1.3.6.1.4.1.6729.2.1.1.4.1.1.3.0 (Show player package) to 1.3.6.1.4.1.6729.2.1.1.3.1.1.3.0 (Show Store package) This correaltes to software version as reported by software 

- The following monitoring types had thresholds multiplied X 10 (Ticket LJF-18)
  - Temperature_ICP_Board
  - Temperature_ICP_FPGA
  - Temperature_FMT_FPGA 

9. Wanda_json_100_v9
    ```
    v9 22/12/2016
- monitoring type names changed for LG reporting

8. Wanda_json_100_v8
    ```
    V8 21/12/2016
- Lamp_Expired threshold added 1 = expired

7. Wanda_json_100_v7
    ```
    V7 20/12/2016
- NEC lamp names changed to
  - Lamp_life
  - Lamp_Hours

6. Wanda_json_100_v6
    ```
    V6 20/12/2016
- NEC models snmp version set to version 1 

5. Wanda_json_100_v5
    ```
    V5 19/12/2016
- NEC models updated to match screenwriter models Series 2.

4. Wanda_json_100_v4
    ```
    V4
- V4- NEC S1 nd S2 added

3. Wanda_json_100_v3
    ```
    V3 15122016
- Changed Lamp_Current_Lamp_Hours to Lanmp_Hours so it is consistent with other projector monitoring types (consistent naming convention across devices) 

2. Wanda_json_100_v2
    ```
    V2 15122016
- Added 1.3.6.1.4.1.25766.1.11.10.4.3.0 oid  to Lamp_Current_Lamp_Hours for series 1 projectors 

1. Major re-working for Wanda
    ```
    v1 13122016
- Increased polling frequency (required for performance) 
- Reduced Monitoring Types (required for performance)  
- Removed AAM_ prefix 
- GDC added
- Dolby CP750 added 
- IMS added

0.9. Major Re-working completed
- VOX_Master_v9 uploade JSON file is edited to accommodate a number of restrictions inherent to Lifeguard V1.12
* `Peeping Tom ---- Any conflicting oids with the peeping tom file have been removed this is to address misreporting this causes at Screenwriter and to avoid duplicating data on Lifeguard.
* `Transformers -----The inability to convert integers to strings means that in cases where this provides info only they have not been included in the JSON file. 
* `Integrer transformers --- Where integers are used to reflect status and used in threshold management a supplement document has been provided with a description of the transformers.
* `Thresholds---Whenever possible a master threshold has been identified and thresholds refined as much as possible to reduce false reporting when a projector is powered off. There are an expected number of critical alerts generated when a projector is powered off or in standby.

0.8. Original monitoring_configuration File
**Common to both Wanda and Vox as of 13/10/2016**



