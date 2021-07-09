https://github.com/elastic/elasticsearch/issues/24874


let  body1  = await client.search({
      index: 'auditlogs*',
    body: {
        size: 20,
        from: 0,
        sort: [
            {
               '@timestamp': {
                    'order': 'asc'
                }
            }
        ],
        "query": {
        "range": {
            "@timestamp": {
                "gte": "2017-05||/M",
                    "format": "yyyy-MM"
            }
        }
    }
    }}, (err, result) => {
        if (err) console.log(err)
      if (result) console.log(result)
    });
    
    
    
    
    

{
      index: 'auditlogs*',
    body: {
        size: 20,
        from: 0,
        sort: [
            {
               '@timestamp': {
                    'order': 'asc'
                }
            }
        ],
            query: {
            bool: {
                should: [
                    {
                        match: {
                            'fields.meta.engine' : 'googlse'
                        }
                    },
                    {
                        match: {
                            'message' : 'GET /v1/realtimeinsightsapi/status 304 3ms'
                        }
                    }

                ]
            }
        }
    }




    {
        size: 20,
        from: 0,
        sort: [
            {
               '@timestamp': {
                    'order': 'asc'
                }
            }
        ],
            query: {
            bool: {
                should: [
                    {
                        match: {
                            'fields.identityId' : '7448425a6735487a4b484f6d33344c4c684252614d4273374474673147354c6c'
                        }
                    }

                ]
            }
        }
    }
