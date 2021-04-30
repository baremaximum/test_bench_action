FROM rust:1.51

# Create and change working directory

WORKDIR /app

# Install nightly toolchain
RUN rustup toolchain install nightly

# Switch to nightly rust
RUN rustup override set nightly

# Copy source
COPY . .

# Remove this
RUN ls -a

# Copy cargo manifest
COPY Cargo.toml Cargo.toml

# Copy entrypoint
COPY ./.github/actions/entrypoint.sh entrypoint.sh

# Make entrypoint executable
RUN chmod +x entrypoint.sh

# Set Entrypoint
ENTRYPOINT [ "entrypoint.sh" ]

