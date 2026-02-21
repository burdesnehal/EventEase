FROM node:20-alpine AS base
WORKDIR /app
RUN apk add --no-cache dumb-init
COPY package*.json ./

FROM base AS dependencies
RUN npm ci --only=production

FROM base AS development
ENV NODE_ENV=development
RUN npm install
COPY . .
EXPOSE 5000
CMD ["dumb-init", "node", "app.js"]

FROM base AS production
ENV NODE_ENV=production
RUN addgroup -g 1001 -S nodejs && \
    adduser -S nodeuser -u 1001
COPY --from=dependencies /app/node_modules ./node_modules
COPY . .
RUN chown -R nodeuser:nodejs /app
USER nodeuser
EXPOSE 5000
CMD ["dumb-init", "node", "app.js"]
