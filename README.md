# Python Protocol Buffer Stubs

Generated Python stubs for Movie Platform gRPC services.

## Overview
This package contains auto-generated Python classes from Protocol Buffer definitions for the Movie Platform microservices architecture.

## Generated Services
- **Common**: Base request/response patterns, error handling, pagination, common types
- **User**: User management, profiles, preferences, watchlists, ratings, history
- **Auth**: Authentication, registration, sessions, tokens, permissions, MFA
- **Movie**: Movie content, search, media assets, catalog, streaming metadata
- **Recommendation**: ML-based recommendations, behavior analysis, content similarity
- **Playback**: Streaming management, progress tracking, quality adaptation
- **Notification**: User notifications, email, push, marketing communications

## Installation
```bash
pip install -e .
```

## Dependencies Required
```python
install_requires=[
    "grpcio>=1.64.0",
    "grpcio-tools>=1.64.0",
    "protobuf>=4.25.0",
]
```

## Usage Example
```python
from proto.common.base_request_pb2 import BaseRequest
from proto.user.user_req_res_pb2 import CreateUserRequest

# Create base request
base_request = BaseRequest(
    request_id="req-123",
    auth_token="jwt-token"
)

# Use in service calls
request = CreateUserRequest(
    base_request=base_request,
    username="john_doe",
    email="john@example.com"
)
```

## Package Structure
```
proto/
├── common/          # Base types, error handling, pagination
├── user/            # User management services
├── auth/            # Authentication services
├── movie/           # Movie content services
├── recommendation/  # Recommendation engine services
├── playback/        # Streaming services
└── notification/    # Notification services
```

## Regeneration
To regenerate these stubs, run from the project root:
```bash
./proto/generate_proto.sh --python-only
```

## Notes
- Generated from Protocol Buffer definitions in `proto/` directory
- Uses Protocol Buffers v4.30.2
- Compatible with gRPC v1.64.0
- All services follow consistent naming conventions
- Includes comprehensive error handling and validation
