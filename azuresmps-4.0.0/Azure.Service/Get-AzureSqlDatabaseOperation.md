---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099523"
---
# <span data-ttu-id="f0c5d-101">Get-AzureSqlDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="f0c5d-101">Get-AzureSqlDatabaseOperation</span></span>

## <span data-ttu-id="f0c5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c5d-103">Hämtar statusen för databas åtgärder på en Azure-Server.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-103">Gets the status of database operations on an Azure server.</span></span>

## <span data-ttu-id="f0c5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0c5d-104">SYNTAX</span></span>

### <span data-ttu-id="f0c5d-105">ByConnectionContext (standard)</span><span class="sxs-lookup"><span data-stu-id="f0c5d-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f0c5d-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="f0c5d-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f0c5d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0c5d-107">DESCRIPTION</span></span>
<span data-ttu-id="f0c5d-108">Cmdleten **Get-AzureSqlDatabaseOperation** får statusen för databas åtgärder på den angivna Azure-servern.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-108">The **Get-AzureSqlDatabaseOperation** cmdlet gets the status of database operations on the specified Azure server.</span></span>
<span data-ttu-id="f0c5d-109">Om du bara anger parametern *Server namn* eller *ConnectionContext* , får cmdleten alla databas operationer för servern.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-109">If you specify only the *ServerName* or *ConnectionContext* parameter, the cmdlet gets all the database operations for the server.</span></span>
<span data-ttu-id="f0c5d-110">Om du också anger en databas med parametern *databas* eller *databasename* får denna cmdlet alla åtgärder för den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-110">If you also specify a database by using the *Database* or *DatabaseName* parameter, this cmdlet gets all the operations for the specified database.</span></span>
<span data-ttu-id="f0c5d-111">Om du anger ett åtgärds-GUID och *Server namn* eller *ConnectionContext* , får cmdleten en enda databas operation.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-111">If you specify an operation GUID, and *ServerName* or *ConnectionContext* , the cmdlet gets a single database operation.</span></span>

## <span data-ttu-id="f0c5d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0c5d-112">EXAMPLES</span></span>

### <span data-ttu-id="f0c5d-113">Exempel 1: få status för alla databas åtgärder för en databas</span><span class="sxs-lookup"><span data-stu-id="f0c5d-113">Example 1: Get the status of all database operations for a database</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

<span data-ttu-id="f0c5d-114">Det här kommandot får statusen för alla databas åtgärder på databasen som heter Database17 på den server som kontexten för anslutning $Context anger.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-114">This command gets the status of all database operations on the database named Database17 on the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="f0c5d-115">Exempel 2: få status för alla databas åtgärder för en server</span><span class="sxs-lookup"><span data-stu-id="f0c5d-115">Example 2: Get the status of all database operations for a server</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

<span data-ttu-id="f0c5d-116">Det här kommandot får statusen för alla databas åtgärder på den server som kontexten $Context anger.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-116">This command gets the status of all database operations on the server that the connection context $Context specifies.</span></span>

## <span data-ttu-id="f0c5d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0c5d-117">PARAMETERS</span></span>

### <span data-ttu-id="f0c5d-118">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="f0c5d-118">-ConnectionContext</span></span>
<span data-ttu-id="f0c5d-119">Anger en servers anslutning.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c5d-120">-Databas</span><span class="sxs-lookup"><span data-stu-id="f0c5d-120">-Database</span></span>
<span data-ttu-id="f0c5d-121">Anger ett objekt som representerar en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-121">Specifies an object that represents an Azure SQL Database.</span></span>
<span data-ttu-id="f0c5d-122">Om du anger den här parametern måste du ange parametern *Server namn* eller parametern *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="f0c5d-122">If you specify this parameter, you must specify the *ServerName* parameter or *ConnectionContext* parameter.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c5d-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f0c5d-123">-DatabaseName</span></span>
<span data-ttu-id="f0c5d-124">Anger namnet på en databas.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-124">Specifies the name of a database.</span></span>
<span data-ttu-id="f0c5d-125">Om du anger den här parametern måste du ange parametern *Server namn* eller parametern *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="f0c5d-125">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c5d-126">-OperationGuid</span><span class="sxs-lookup"><span data-stu-id="f0c5d-126">-OperationGuid</span></span>
<span data-ttu-id="f0c5d-127">Anger det åtgärds-ID som representerar en specifik databas åtgärd för vilken denna cmdlet får status.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-127">Specifies the operation ID that represents a specific database operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="f0c5d-128">Du kan skaffa åtgärds-ID genom att begära alla databas åtgärder för en Azure SQL-databas eller-server.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-128">You can obtain operation IDs by requesting all the database operations for a Azure SQL Database or server.</span></span>
<span data-ttu-id="f0c5d-129">Om du anger den här parametern måste du ange parametern *Server namn* eller parametern *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="f0c5d-129">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c5d-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="f0c5d-130">-Profile</span></span>
<span data-ttu-id="f0c5d-131">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f0c5d-132">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c5d-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f0c5d-133">-ServerName</span></span>
<span data-ttu-id="f0c5d-134">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-134">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c5d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c5d-135">CommonParameters</span></span>
<span data-ttu-id="f0c5d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c5d-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c5d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c5d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0c5d-138">INPUTS</span></span>

### <span data-ttu-id="f0c5d-139">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="f0c5d-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="f0c5d-140">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="f0c5d-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

### <span data-ttu-id="f0c5d-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f0c5d-141">System.Guid</span></span>

## <span data-ttu-id="f0c5d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0c5d-142">OUTPUTS</span></span>

### <span data-ttu-id="f0c5d-143">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database. DatabaseOperationResponseList []</span><span class="sxs-lookup"><span data-stu-id="f0c5d-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponseList[]</span></span>
<span data-ttu-id="f0c5d-144">Denna cmdlet returnerar en matris med **DatabaseOperationResponseList** -objekt om du får flera operationer.</span><span class="sxs-lookup"><span data-stu-id="f0c5d-144">This cmdlet returns an array of **DatabaseOperationResponseList** objects if you get multiple operations.</span></span>

### <span data-ttu-id="f0c5d-145">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database. DatabaseOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f0c5d-145">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponse</span></span>

## <span data-ttu-id="f0c5d-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0c5d-146">NOTES</span></span>

## <span data-ttu-id="f0c5d-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0c5d-147">RELATED LINKS</span></span>

[<span data-ttu-id="f0c5d-148">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="f0c5d-148">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="f0c5d-149">Databas åtgärds status</span><span class="sxs-lookup"><span data-stu-id="f0c5d-149">Database Operation Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[<span data-ttu-id="f0c5d-150">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="f0c5d-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f0c5d-151">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f0c5d-151">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="f0c5d-152">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="f0c5d-152">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


