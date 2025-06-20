<link rel="stylesheet" href="smol-slimes.css">

# Pre-Compiled Firmware for Default Pins

```admonish important
This is the recommended method of getting the firmware if you don't need custom config or pin defines.
```

### Required Tools

You only need the following if you are using precompiled firmware:
* <a href="https://www.nordicsemi.com/Products/Development-tools/nRF-Connect-for-Desktop">nRF Connect for Desktop</a> (Programmer) for flashing Nordic or eByte Dongles only
* <a href="https://www.nordicsemi.com/Products/Development-tools/nRF-Connect-for-Desktop">nRF Connect for Desktop</a> (Serial Terminal) for sending commands to your Receiver/Trackers, [see alternatives](#accessing-the-serial-console)
* <a href="https://slimevr.dev/download">SlimeVR Server</a>
    * 0.13.2 or later version

### Latest Builds (Automated)

#### 💿 Adafruit Bootloader
| Device               | UF2 | HEX |
| ------------------ | ---- | ---- |
| ProMicro/SuperMini | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/update-slimenrf_promicro_bootloader-0.9.2-SlimeVR.6_nosd.uf2) | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/slimenrf_promicro_bootloader-0.9.2-SlimeVR.6_s140_7.3.0.hex) |
| XIAO | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/update-slimenrf_xiao_sense_bootloader-0.9.2-SlimeVR.6_nosd.uf2) | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/slimenrf_xiao_sense_bootloader-0.9.2-SlimeVR.6_s140_7.3.0.hex) |
| R3 | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/update-slimenrf_tracker_r3_bootloader-0.9.2-SlimeVR.6_nosd.uf2) | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/slimenrf_tracker_r3_bootloader-0.9.2-SlimeVR.6_s140_7.3.0.hex) |
| SlimeVR Mini P1 | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/update-slimevr_mini_p1_bootloader-0.9.2-SlimeVR.6_nosd.uf2) | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/slimevr_mini_p1_bootloader-0.9.2-SlimeVR.6_s140_7.3.0.hex) |
| SlimeVR Mini P2 | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/update-slimevr_mini_p2_bootloader-0.9.2-SlimeVR.6_nosd.uf2) | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/slimevr_mini_p2_bootloader-0.9.2-SlimeVR.6_s140_7.3.0.hex) |
| SlimeVR Mini P3, R6| [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/update-slimevr_mini_p3r6_bootloader-0.9.2-SlimeVR.6_nosd.uf2) | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/slimevr_mini_p3r6_bootloader-0.9.2-SlimeVR.6_s140_7.3.0.hex) |
| SlimeVR Mini P3, R7 | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/update-slimevr_mini_p3r7_bootloader-0.9.2-SlimeVR.6_nosd.uf2) | [Link](https://github.com/SlimeVR/Adafruit_nRF52_Bootloader/releases/download/0.9.2-SlimeVR.6/slimevr_mini_p3r7_bootloader-0.9.2-SlimeVR.6_s140_7.3.0.hex) |

#### 📡 Receiver

| Device       | Download                                                                                                                             |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| Nordic/eByte | [Link](https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Nordic_eByte_Dongle_Receiver.hex) |
| Holyiot      | [Link](https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Holyiot_Dongle_Receiver.hex)      |
| SuperMini    | [Link](https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_SuperMini_Receiver.uf2)           |
| XIAO         | [Link](https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_XIAO_Receiver.uf2)                |

#### 🏃 Tracker

<div class="table-wrapper">
  <table>
    <thead>
      <tr>
        <th>Device</th>
        <th>Protocol</th>
        <th>Stacked</th>
        <th>Clock (ICM)</th>
        <th>
          Sleep
          <span class="tooltip-text-container">
            (WOM)
            <span class="tooltip-text"> Wake On Motion. </span>
          </span>
        </th>
        <th>
            SW0 Disabled
            <br/>
            (no button)
        </th>
        <th>
            SW0 Enabled
            <br/>
            (button)
        </th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>SuperMini</td>
        <td>SPI</td>
        <td>✖️</td>
        <td>✖️</td>
        <td>✅</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SPI_SuperMini.uf2"
            >Link</a
          >
        </td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SW0_SPI_SuperMini.uf2"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>SuperMini</td>
        <td>SPI</td>
        <td>✖️</td>
        <td>✖️</td>
        <td>✖️</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleep_SPI_SuperMini.uf2"
            >Link</a
          >
        </td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SW0_NoSleep_SPI_SuperMini.uf2"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>SuperMini</td>
        <td>SPI</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✅</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_CLK_SPI_SuperMini.uf2"
            >Link</a
          >
        </td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SW0_CLK_SPI_SuperMini.uf2"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>SuperMini</td>
        <td>SPI</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✖️</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleepCLK_SPI_SuperMini.uf2"
            >Link</a
          >
        </td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SW0_NoSleepCLK_SPI_SuperMini.uf2"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>SuperMini</td>
        <td>I2C</td>
        <td>✖️</td>
        <td>✖️</td>
        <td>✅</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_I2C_SuperMini.uf2"
            >Link</a
          >
        </td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SW0_I2C_SuperMini.uf2"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>SuperMini</td>
        <td>I2C</td>
        <td>✖️</td>
        <td>✖️</td>
        <td>✖️</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleep_I2C_SuperMini.uf2"
            >Link</a
          >
        </td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SW0_NoSleep_I2C_SuperMini.uf2"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>SuperMini</td>
        <td>I2C</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✅</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_CLK_I2C_SuperMini.uf2"
            >Link</a
          >
        </td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SW0_CLK_I2C_SuperMini.uf2"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>SuperMini</td>
        <td>I2C</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✖️</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleepCLK_I2C_SuperMini.uf2"
            >Link</a
          >
        </td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SW0_NoSleepCLK_I2C_SuperMini.uf2"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>SuperMini</td>
        <td>SPI</td>
        <td>🥪</td>
        <td>✅</td>
        <td>✅</td>
        <td>N/A</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SPI_StackedSmol.uf2"
            target="_blank"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>SuperMini</td>
        <td>SPI</td>
        <td>🥪</td>
        <td>✅</td>
        <td>✖️</td>
        <td>N/A</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleep_SPI_StackedSmol.uf2"
            target="_blank"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>SuperMini</td>
        <td>I2C</td>
        <td>🥪</td>
        <td>✅</td>
        <td>✅</td>
        <td>N/A</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_I2C_StackedSmol.uf2"
            target="_blank"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>SuperMini</td>
        <td>I2C</td>
        <td>🥪</td>
        <td>✅</td>
        <td>✖️</td>
        <td>N/A</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleep_I2C_StackedSmol.uf2"
            target="_blank"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>XIAO</td>
        <td>I2C/SPI</td>
        <td>✖️</td>
        <td>✖️</td>
        <td>✅</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_XIAO.uf2"
            >Link</a
          >
        </td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SW0_XIAO.uf2"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>XIAO</td>
        <td>I2C/SPI</td>
        <td>✖️</td>
        <td>✖️</td>
        <td>✖️</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleep_XIAO.uf2"
            >Link</a
          >
        </td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SW0_NoSleep_XIAO.uf2"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>XIAO</td>
        <td>I2C/SPI</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✅</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_CLK_XIAO.uf2"
            >Link</a
          >
        </td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SW0_CLK_XIAO.uf2"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>XIAO</td>
        <td>I2C/SPI</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✖️</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleepCLK_XIAO.uf2"
            >Link</a
          >
        </td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SW0_NoSleepCLK_XIAO.uf2"
            >Link</a
          >
        </td>
      </tr>
      <tr>
        <td>R3</td>
        <td>I2C</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✅</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_R3.uf2"
            >Link</a
          >
        </td>
        <td>N/A</td>
      </tr>
      <tr>
        <td>R3</td>
        <td>I2C</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✖️</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleep_R3.uf2"
            >Link</a
          >
        </td>
        <td>N/A</td>
      </tr>
      <tr>
        <td>SlimeVR Mini (P1)</td>
        <td>I2C</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✅</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SlimevrMini.uf2"
            >Link</a
          >
        </td>
        <td>N/A</td>
      </tr>
      <tr>
        <td>SlimeVR Mini (P1)</td>
        <td>I2C</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✖️</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleep_SlimevrMini.uf2"
            >Link</a
          >
        </td>
        <td>N/A</td>
      </tr>
      <tr>
        <td>SlimeVR Mini (P2)</td>
        <td>I2C</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✅</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_SlimevrMini2.uf2"
            >Link</a
          >
        </td>
        <td>N/A</td>
      </tr>
      <tr>
        <td>SlimeVR Mini (P2)</td>
        <td>I2C</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✖️</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleep_SlimevrMini2.uf2"
            >Link</a
          >
        </td>
        <td>N/A</td>
      </tr>
      <tr>
        <td>SlimeVR Mini (P3, R6)</td>
        <td>I2C</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✖️</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleep_SlimevrMini3_R6.uf2"
            >Link</a
          >
        </td>
        <td>N/A</td>
      </tr>
      <tr>
        <td>SlimeVR Mini (P3, R7)</td>
        <td>I2C</td>
        <td>✖️</td>
        <td>✅</td>
        <td>✖️</td>
        <td>
          <a
            href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/releases/download/latest/SlimeNRF_Tracker_NoSleep_SlimevrMini3_R7.uf2"
            >Link</a
          >
        </td>
        <td>N/A</td>
      </tr>
    </tbody>
  </table>
</div>

#### Previous Firmware Builds

Previous builds can be found here: <a href="https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/actions">https://github.com/Shine-Bright-Meow/SlimeNRF-Firmware-CI/actions</a>

1. Click on a successful workflow run ✅ for the specified date range.
2. Scroll down to the **Artifacts** section.
3. Download the desired device firmware.
4. Extract the ZIP file.

*Created by Shine Bright ✨, [Depact](https://github.com/Depact) and [Seneral](https://github.com/Seneral)*
