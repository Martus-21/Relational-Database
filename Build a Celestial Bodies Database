--
-- PostgreSQL database dump
--

-- Dumped from database version 12.17 (Ubuntu 12.17-1.pgdg22.04+1)
-- Dumped by pg_dump version 12.17 (Ubuntu 12.17-1.pgdg22.04+1)

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

DROP DATABASE universe;
--
-- Name: universe; Type: DATABASE; Schema: -; Owner: freecodecamp
--

CREATE DATABASE universe WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'C.UTF-8' LC_CTYPE = 'C.UTF-8';


ALTER DATABASE universe OWNER TO freecodecamp;

\connect universe

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- Name: comet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.comet (
    comet_id integer NOT NULL,
    name character varying(255) NOT NULL,
    orbit_period integer NOT NULL,
    origin character varying(255) NOT NULL,
    has_tail boolean NOT NULL
);


ALTER TABLE public.comet OWNER TO freecodecamp;

--
-- Name: comet_comet_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.comet_comet_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.comet_comet_id_seq OWNER TO freecodecamp;

--
-- Name: comet_comet_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.comet_comet_id_seq OWNED BY public.comet.comet_id;


--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    name character varying(255) NOT NULL,
    description text,
    galaxy_type character varying(50) NOT NULL,
    distance_from_earth numeric NOT NULL,
    has_life boolean NOT NULL
);


ALTER TABLE public.galaxy OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_galaxy_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_galaxy_id_seq OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_galaxy_id_seq OWNED BY public.galaxy.galaxy_id;


--
-- Name: moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.moon (
    moon_id integer NOT NULL,
    name character varying(255) NOT NULL,
    planet_id integer,
    diameter_in_km numeric NOT NULL,
    is_habitable boolean NOT NULL,
    composition text NOT NULL
);


ALTER TABLE public.moon OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.moon_moon_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.moon_moon_id_seq OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.moon_moon_id_seq OWNED BY public.moon.moon_id;


--
-- Name: planet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet (
    planet_id integer NOT NULL,
    name character varying(255) NOT NULL,
    star_id integer,
    planet_type character varying(50) NOT NULL,
    has_life boolean NOT NULL,
    is_spherical boolean NOT NULL
);


ALTER TABLE public.planet OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_planet_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_planet_id_seq OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_planet_id_seq OWNED BY public.planet.planet_id;


--
-- Name: star; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star (
    star_id integer NOT NULL,
    name character varying(255) NOT NULL,
    galaxy_id integer,
    star_type character varying(50) NOT NULL,
    age_in_millions_of_years integer NOT NULL,
    is_bright boolean NOT NULL
);


ALTER TABLE public.star OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_star_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_star_id_seq OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_star_id_seq OWNED BY public.star.star_id;


--
-- Name: comet comet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.comet ALTER COLUMN comet_id SET DEFAULT nextval('public.comet_comet_id_seq'::regclass);


--
-- Name: galaxy galaxy_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy ALTER COLUMN galaxy_id SET DEFAULT nextval('public.galaxy_galaxy_id_seq'::regclass);


--
-- Name: moon moon_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon ALTER COLUMN moon_id SET DEFAULT nextval('public.moon_moon_id_seq'::regclass);


--
-- Name: planet planet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet ALTER COLUMN planet_id SET DEFAULT nextval('public.planet_planet_id_seq'::regclass);


--
-- Name: star star_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star ALTER COLUMN star_id SET DEFAULT nextval('public.star_star_id_seq'::regclass);


--
-- Data for Name: comet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.comet VALUES (1, 'Halley Comet', 75, 'Kuiper Belt', true);
INSERT INTO public.comet VALUES (2, 'Hale-Bopp', 2533, 'Oort Cloud', true);
INSERT INTO public.comet VALUES (3, 'Encke Comet', 3, 'Kuiper Belt', true);


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES (1, 'Milky Way', 'Our galaxy', 'Spiral', 0, true);
INSERT INTO public.galaxy VALUES (2, 'Andromeda', 'Nearest spiral galaxy', 'Spiral', 2537000, false);
INSERT INTO public.galaxy VALUES (3, 'Triangulum', 'A member of the Local Group', 'Spiral', 3000000, false);
INSERT INTO public.galaxy VALUES (4, 'Whirlpool', 'Famous for its spiral structure', 'Spiral', 23000000, false);
INSERT INTO public.galaxy VALUES (5, 'Messier 87', 'A giant elliptical galaxy', 'Elliptical', 53000000, false);
INSERT INTO public.galaxy VALUES (6, 'Sombrero', 'Notable for its bright nucleus', 'Elliptical', 29000000, false);


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES (1, 'Luna', 1, 3474.2, false, 'Rock');
INSERT INTO public.moon VALUES (2, 'Europa', 5, 3122, false, 'Ice');
INSERT INTO public.moon VALUES (3, 'Ganymede', 5, 5268, false, 'Rock');
INSERT INTO public.moon VALUES (4, 'Callisto', 5, 4820, false, 'Rock');
INSERT INTO public.moon VALUES (5, 'Titan', 6, 5149, false, 'Ice');
INSERT INTO public.moon VALUES (6, 'Enceladus', 6, 504, false, 'Ice');
INSERT INTO public.moon VALUES (7, 'Io', 5, 3642, false, 'Rock');
INSERT INTO public.moon VALUES (8, 'Phobos', 2, 22.4, false, 'Rock');
INSERT INTO public.moon VALUES (9, 'Deimos', 2, 12.4, false, 'Rock');
INSERT INTO public.moon VALUES (10, 'Mimas', 6, 396, false, 'Ice');
INSERT INTO public.moon VALUES (11, 'Triton', 8, 2706, false, 'Ice');
INSERT INTO public.moon VALUES (12, 'Nereid', 8, 340, false, 'Rock');
INSERT INTO public.moon VALUES (13, 'Charon', 4, 1212, false, 'Rock');
INSERT INTO public.moon VALUES (14, 'Dysnomia', 4, 700, false, 'Rock');
INSERT INTO public.moon VALUES (15, 'Titania', 7, 1578, false, 'Rock');
INSERT INTO public.moon VALUES (16, 'Oberon', 7, 1523, false, 'Rock');
INSERT INTO public.moon VALUES (17, 'Umbriel', 7, 1169, false, 'Rock');
INSERT INTO public.moon VALUES (18, 'Ariel', 7, 1158, false, 'Rock');
INSERT INTO public.moon VALUES (19, 'Miranda', 7, 471.6, false, 'Rock');
INSERT INTO public.moon VALUES (20, 'Proteus', 8, 418, false, 'Rock');


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (1, 'Tatooine', 1, 'Desert', false, true);
INSERT INTO public.planet VALUES (2, 'Hoth', 2, 'Ice', false, true);
INSERT INTO public.planet VALUES (3, 'Dagobah', 2, 'Swamp', true, true);
INSERT INTO public.planet VALUES (4, 'Endor', 3, 'Forest', true, true);
INSERT INTO public.planet VALUES (5, 'Mustafar', 4, 'Volcanic', false, true);
INSERT INTO public.planet VALUES (6, 'Naboo', 4, 'Terrestrial', true, true);
INSERT INTO public.planet VALUES (7, 'Kamino', 5, 'Ocean', false, true);
INSERT INTO public.planet VALUES (8, 'Geonosis', 5, 'Rocky', false, true);
INSERT INTO public.planet VALUES (9, 'Kashyyyk', 6, 'Jungle', true, true);
INSERT INTO public.planet VALUES (10, 'Coruscant', 6, 'Urban', true, true);
INSERT INTO public.planet VALUES (11, 'Bespin', 1, 'Gas Giant', false, true);
INSERT INTO public.planet VALUES (12, 'Polis Massa', 3, 'Asteroid', false, true);


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--
