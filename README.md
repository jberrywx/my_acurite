SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET time_zone = "+00:00";

--
-- Database: `my_acurite`
--

-- --------------------------------------------------------

--
-- Table structure for table `mystation`
--

CREATE TABLE IF NOT EXISTS `mystation` (
  `ID` int(11) NOT NULL,
  `DateTime` datetime NOT NULL COMMENT 'Date and Time of Readings',
  `TempOutCur` decimal(4,1) NOT NULL COMMENT 'Current Outdoor Temperature',
  `HumOutCur` int(11) NOT NULL COMMENT 'Current Outdoor Humidity',
  `PressCur` decimal(4,2) NOT NULL COMMENT 'Current Barometric Pressure',
  `DewCur` decimal(4,1) NOT NULL COMMENT 'Current Dew Point',
  `HeatIdxCur` decimal(4,1) NOT NULL COMMENT 'Current Heat Index',
  `WindChillCur` decimal(4,1) NOT NULL COMMENT 'Current Wind Chill',
  `TempInCur` decimal(4,1) NOT NULL COMMENT 'Current Indoor Temperature',
  `HumInCur` int(11) NOT NULL COMMENT 'Current Indoor Humidity',
  `WindSpeedCur` decimal(4,1) NOT NULL COMMENT 'Current Wind Speed',
  `WindAvgSpeedCur` decimal(4,1) NOT NULL COMMENT 'Current Average Wind Speed',
  `WindDirCur` int(11) NOT NULL COMMENT 'Current Wind Direction (Degrees)',
  `WindDirCurEng` varchar(3) NOT NULL COMMENT 'Current Wind Direction (English)',
  `WindGust10` decimal(4,1) NOT NULL COMMENT 'Max Wind Gust for Past 10 Mins',
  `WindDirAvg10` int(11) NOT NULL COMMENT 'Average Wind Direction (Degrees) for Past 10 Mins',
  `WindDirAvg10Eng` varchar(3) NOT NULL COMMENT 'Average Wind Direction (English) for Past 10 Mins',
  `RainRateCur` decimal(5,2) NOT NULL COMMENT 'Current Rain Rate',
  `RainDay` decimal(4,2) NOT NULL COMMENT 'Total Rain for Today',
  `RainYest` decimal(4,2) NOT NULL COMMENT 'Total Rain for Yesterday',
  `RainMonth` decimal(5,2) NOT NULL COMMENT 'Total Rain this Month',
  `RainYear` decimal(5,2) NOT NULL COMMENT 'Total Rain this Year'
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `mystation`=
-- INSERT INTO `my_acurite`.`mystation` (`ID`, `DateTime`, `TempOutCur`, `HumOutCur`, `PressCur`, `DewCur`, `HeatIdxCur`, `WindChillCur`, `TempInCur`, `HumInCur`, `WindSpeedCur`, `WindAvgSpeedCur`, `WindDirCur`, `WindDirCurEng`, `WindGust10`, `WindDirAvg10`, `WindDirAvg10Eng`, `RainRateCur`, `RainDay`, `RainYest`, `RainMonth`, `RainYear`) VALUES (NULL, '[YYYY]-[MM]-[DD] [hh]:[mm]:[ss]', '[th0temp-act=F]', '[th0hum-act]', '[thb0seapress-act=inHg.2]', '[th0dew-act=F]', '[th0heatindex-act=F]', '[wind0chill-act=F]', '[thb0temp-act=F]', '[thb0hum-act]', '[wind0wind-act=mph]', '[wind0avgwind-act=mph]', '[wind0dir-act]', '[wind0dir-act=endir]', '[wind0wind-max10=mph]', '[wind0dir-avg10]', '[wind0dir-avg10=endir]', '[rain0rate-act=in.2]', '[rain0total-daysum=in.2]', '[rain0total-ydaysum=in.2]', '[rain0total-monthsum=in.2]', '[rain0total-yearsum=in.2]')

INSERT INTO `mystation` (`ID`, `DateTime`, `TempOutCur`, `HumOutCur`, `PressCur`, `DewCur`, `HeatIdxCur`, `WindChillCur`, `TempInCur`, `HumInCur`, `WindSpeedCur`, `WindAvgSpeedCur`, `WindDirCur`, `WindDirCurEng`, `WindGust10`, `WindDirAvg10`, `WindDirAvg10Eng`, `RainRateCur`, `RainDay`, `RainYest`, `RainMonth`, `RainYear`) VALUES
(1, '2015-02-12 22:00:00', '54.7', 78, '30.24', '48.0', '54.7', '54.7', '79.0', 40, '0.9', '0.0', 134, 'SE', '2.0', 142, 'SE', '0.00', '0.03', '0.01', '4.54', '10.12');

--
-- Indexes for table `mystation`
--
ALTER TABLE `mystation`
  ADD PRIMARY KEY (`ID`);

--
-- AUTO_INCREMENT for table `mystation`
--
ALTER TABLE `mystation`
  MODIFY `ID` int(11) NOT NULL AUTO_INCREMENT,AUTO_INCREMENT=1;
