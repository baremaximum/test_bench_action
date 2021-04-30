FROM rust:1.51

# Switch to nightly rust
RUN rustup override set nightly

# Copy source
COPY . .

# Copy entrypoint
COPY entrypoint.sh /entrypoint.sh

# Make entrypoint executable
RUN chmod +x entrypoint.sh

RUN echo "${PATH}"

# Set Entrypoint
ENTRYPOINT [ "/entrypoint.sh"]

