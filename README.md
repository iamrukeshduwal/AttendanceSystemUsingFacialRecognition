# AttendanceSystemUsingFacialRecognition
-- phpMyAdmin SQL Dump
-- version 4.8.5
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Generation Time: Sep 06, 2022 at 06:46 PM
-- Server version: 10.1.39-MariaDB
-- PHP Version: 7.3.5

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET AUTOCOMMIT = 0;
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `face_recognition`
--

-- --------------------------------------------------------

--
-- Table structure for table `regteach`
--

CREATE TABLE `regteach` (
  `fname` varchar(45) NOT NULL,
  `lname` varchar(45) NOT NULL,
  `cnum` varchar(45) NOT NULL,
  `email` varchar(45) NOT NULL,
  `ss_que` varchar(45) NOT NULL,
  `s_ans` varchar(45) NOT NULL,
  `pwd` varchar(45) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `regteach`
--

INSERT INTO `regteach` (`fname`, `lname`, `cnum`, `email`, `ss_que`, `s_ans`, `pwd`) VALUES
('b', 'b', 'b', 'b', 'Your Date of Birth', 'b', 'b'),
('Dibas', 'Chalise', '**********', 'dibase@gmail.com', 'Your Favorite Book', 'book', '2'),
('Bibek', 'Duwal', '**********', 'iambibekduwal@gmail.com', 'Your Date of Birth', '2000', '123456'),
('Rukesh', 'Duwal', '**********', 'iamrukeshduwal@gmail.com', 'Your Date of Birth', '1998', 'admin'),
('ram', 'thapa', '**********', 'ram123@gmail.com', 'Your Date of Birth', '2000', 'ram'),
('Sanket', 'Tamang', '**********', 'sanket@gmail.com', 'Your Date of Birth', '1999', '1');

-- --------------------------------------------------------

--
-- Table structure for table `stdattendance`
--

CREATE TABLE `stdattendance` (
  `std_id` varchar(45) NOT NULL,
  `std_roll_no` varchar(45) NOT NULL,
  `std_name` varchar(45) NOT NULL,
  `std_time` varchar(45) NOT NULL,
  `std_date` varchar(45) NOT NULL,
  `std_attendance` varchar(45) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `stdattendance`
--

INSERT INTO `stdattendance` (`std_id`, `std_roll_no`, `std_name`, `std_time`, `std_date`, `std_attendance`) VALUES
('1', '1', ' Rukesh Duwal', ' 02:23:15', ' 03/09/2022', ' Present');

-- --------------------------------------------------------

--
-- Table structure for table `student`
--

CREATE TABLE `student` (
  `Student_ID` varchar(45) NOT NULL,
  `Name` varchar(45) NOT NULL,
  `Department` varchar(45) NOT NULL,
  `Course` varchar(45) NOT NULL,
  `Year` varchar(45) NOT NULL,
  `Semester` varchar(45) NOT NULL,
  `Division` varchar(45) NOT NULL,
  `Gender` varchar(45) NOT NULL,
  `DOB` varchar(45) NOT NULL,
  `Mobile_No` varchar(45) NOT NULL,
  `Address` varchar(45) NOT NULL,
  `Roll_No` varchar(45) NOT NULL,
  `Email` varchar(45) NOT NULL,
  `Teacher_Name` varchar(45) NOT NULL,
  `PhotoSample` varchar(45) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `student`
--

INSERT INTO `student` (`Student_ID`, `Name`, `Department`, `Course`, `Year`, `Semester`, `Division`, `Gender`, `DOB`, `Mobile_No`, `Address`, `Roll_No`, `Email`, `Teacher_Name`, `PhotoSample`) VALUES
('1', 'Rukesh duwal', 'Science&Tech', 'BIT', '2017-21', 'Semester-8', 'Morning', 'Male', '1998', '**********', 'Bhaktapur', '1', 'iamrukeshduwal@gmail.com', 'Ram', 'Yes'),
('2', 'dibas chalise', 'Science&Tech', 'BIT', '2017-21', 'Semester-8', 'Morning', 'Male', '1999', '**********', 'kathmandu', '2', 'chalisedibas01@gmail.com', 'Ram', 'Yes');

--
-- Indexes for dumped tables
--

--
-- Indexes for table `regteach`
--
ALTER TABLE `regteach`
  ADD PRIMARY KEY (`email`);

--
-- Indexes for table `stdattendance`
--
ALTER TABLE `stdattendance`
  ADD PRIMARY KEY (`std_id`);

--
-- Indexes for table `student`
--
ALTER TABLE `student`
  ADD PRIMARY KEY (`Student_ID`),
  ADD UNIQUE KEY `Roll_No` (`Roll_No`);
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
