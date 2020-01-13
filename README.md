{
	"info": {
		"_postman_id": "a99dbd70-b800-436e-857e-9b8bb4973e6a",
		"name": "temp-collection",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json"
	},
	"item": [
		{
			"name": "https://www.onliner.by/",
			"event": [
				{
					"listen": "test",
					"script": {
						"id": "f52b360c-dd7f-4a02-ba26-742c2093fd60",
						"exec": [
							"pm.test(\"Response time is less than 200ms\", function () {",
							"    pm.expect(pm.response.responseTime).to.be.below(2000);",
							"pm.test(\"Body matches string\", function () {",
							"    pm.expect(pm.response.text()).to.include(\"Onliner\");",
							"});",
							"});",
							"",
							"pm.test(\"Status code is 200\", function () {",
							"    pm.response.to.have.status(200);",
							"});"
						],
						"type": "text/javascript"
					}
				}
			],
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "https://www.onliner.by/",
					"protocol": "https",
					"host": [
						"www",
						"onliner",
						"by"
					],
					"path": [
						""
					]
				}
			},
			"response": []
		},
		{
			"name": "https://vk.com/feed",
			"event": [
				{
					"listen": "test",
					"script": {
						"id": "eabf32a8-89e4-4609-9e2d-e44dd39ab32e",
						"exec": [
							"",
							"pm.test(\"Body matches string\", function () {",
							"    pm.expect(pm.response.text()).to.include(\"РЈРІР°С…РѕРґ | РЈРљР°РЅС‚Р°РєС†Рµ\");",
							"});",
							"pm.test(\"Status code is 200\", function () {",
							"    pm.response.to.have.status(200);",
							"});",
							"pm.test(\"Status code is 200\", function () {",
							"    pm.response.to.have.status(200);",
							"});"
						],
						"type": "text/javascript"
					}
				}
			],
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "https://vk.com/feed",
					"protocol": "https",
					"host": [
						"vk",
						"com"
					],
					"path": [
						"feed"
					]
				}
			},
			"response": []
		},
		{
			"name": "https://www.tut.by/",
			"event": [
				{
					"listen": "test",
					"script": {
						"id": "c8b777a9-203d-40f9-96f1-30a5011cac60",
						"exec": [
							"pm.test(\"Response time is less than 200ms\", function () {",
							"    pm.expect(pm.response.responseTime).to.be.below(2000);",
							"});",
							"pm.test(\"Body matches string\", function () {",
							"    pm.expect(pm.response.text()).to.include(\"Р‘РµР»РѕСЂСѓСЃСЃРєРёР№ РїРѕСЂС‚Р°Р» TUT.BY. РќРѕРІРѕСЃС‚Рё Р‘РµР»Р°СЂСѓСЃРё Рё РјРёСЂ\");",
							"});",
							"pm.test(\"Status code is 200\", function () {",
							"    pm.response.to.have.status(200);",
							"});"
						],
						"type": "text/javascript"
					}
				}
			],
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "https://www.tut.by/",
					"protocol": "https",
					"host": [
						"www",
						"tut",
						"by"
					],
					"path": [
						""
					]
				}
			},
			"response": []
		}
	],
	"protocolProfileBehavior": {}
}
