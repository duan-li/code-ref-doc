<?php if (!defined('BASEPATH')) exit('No direct script access allowed');

class Home extends Front_Controller {

	public function __construct()
	{
		parent::__construct();

		$this->load->library('users/auth');
		$this->load->helper('form');
	}

	//--------------------------------------------------------------------


	public function index()
	{
		if ($this->auth->is_logged_in())
		{
			redirect('buddies');
		}

		Template::render();
	}

	//--------------------------------------------------------------------

	public function buddies()
	{
		Template::render();
	}

	//--------------------------------------------------------------------

	public function ribbits()
	{
		Template::render();
	}

	//--------------------------------------------------------------------

	public function profiles()
	{
		Template::render();
	}

	//--------------------------------------------------------------------

}