---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099338"
---
# <span data-ttu-id="02b11-101">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="02b11-101">Remove-AzureSqlDatabase</span></span>

## <span data-ttu-id="02b11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02b11-102">SYNOPSIS</span></span>
<span data-ttu-id="02b11-103">Tar bort en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="02b11-103">Deletes an Azure SQL Database.</span></span>

## <span data-ttu-id="02b11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02b11-104">SYNTAX</span></span>

### <span data-ttu-id="02b11-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="02b11-105">ByNameWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b11-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="02b11-106">ByObjectWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b11-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="02b11-107">ByNameWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b11-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="02b11-108">ByObjectWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02b11-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02b11-109">DESCRIPTION</span></span>
<span data-ttu-id="02b11-110">Cmdleten **Remove-AzureSqlDatabase** tar bort en Azure SQL-databas via server anslutnings kontext eller server namn.</span><span class="sxs-lookup"><span data-stu-id="02b11-110">The **Remove-AzureSqlDatabase** cmdlet deletes an Azure SQL Database by server connection context or server name.</span></span>
<span data-ttu-id="02b11-111">Du kan skapa en anslutning till en Azure SQL Database-Server med hjälp av **New-AzureSqlDatabaseServerContext** cmdlet och sedan använda den med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02b11-111">You can create an Azure SQL Database server connection context using the **New-AzureSqlDatabaseServerContext** cmdlet, and then use it with this cmdlet.</span></span>

<span data-ttu-id="02b11-112">När du tar bort en databas genom att ange ett namn på en Azure SQL **-** databasserver används namnet och den aktuella Azure-prenumerations informationen för att utföra åtgärden.</span><span class="sxs-lookup"><span data-stu-id="02b11-112">When you delete a database by specifying an Azure SQL Database server name, the **Remove-AzureSqlDatabase** cmdlet uses the name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="02b11-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02b11-113">EXAMPLES</span></span>

### <span data-ttu-id="02b11-114">Exempel 1: ta bort en databas</span><span class="sxs-lookup"><span data-stu-id="02b11-114">Example 1: Remove a database</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="02b11-115">Det här kommandot tar bort databasen som heter Database01 från $Context för Azure SQL Database Server.</span><span class="sxs-lookup"><span data-stu-id="02b11-115">This command removes the database named Database01 from the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="02b11-116">Exempel 2: ta bort en databas med hjälp av ett server namn</span><span class="sxs-lookup"><span data-stu-id="02b11-116">Example 2: Remove a database by using a server name</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="02b11-117">Det här kommandot tar bort den databas som heter Database01 från en Azure SQL-databasserver som heter lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="02b11-117">This command removes the database named Database01 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="02b11-118">Exempel 3: ta bort en databas genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="02b11-118">Example 3: Remove a database by using the pipeline</span></span>
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="02b11-119">I det här exemplet visas den alternativa metoden för att överföra databasobjektet genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="02b11-119">This example demonstrates the alternative method of passing the database object through the pipeline.</span></span>

## <span data-ttu-id="02b11-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02b11-120">PARAMETERS</span></span>

### <span data-ttu-id="02b11-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="02b11-121">-ConnectionContext</span></span>
<span data-ttu-id="02b11-122">Anger den anslutnings kontext för en server som den här cmdleten tar bort en databas från.</span><span class="sxs-lookup"><span data-stu-id="02b11-122">Specifies the connection context of a server from which this cmdlet removes a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02b11-123">-Databas</span><span class="sxs-lookup"><span data-stu-id="02b11-123">-Database</span></span>
<span data-ttu-id="02b11-124">Anger ett objekt som representerar databasen som tas bort med cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02b11-124">Specifies an object that represents the database that this cmdlet removes.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02b11-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="02b11-125">-DatabaseName</span></span>
<span data-ttu-id="02b11-126">Anger namnet på den databas som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="02b11-126">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b11-127">-Force</span><span class="sxs-lookup"><span data-stu-id="02b11-127">-Force</span></span>
<span data-ttu-id="02b11-128">Gör att åtgärden kan slutföras utan att användaren uppmanas att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="02b11-128">Allows the action to complete without prompting the user for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b11-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="02b11-129">-Profile</span></span>
<span data-ttu-id="02b11-130">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="02b11-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02b11-131">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="02b11-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02b11-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="02b11-132">-ServerName</span></span>
<span data-ttu-id="02b11-133">Anger namnet på den server där cmdleten tar bort databasen.</span><span class="sxs-lookup"><span data-stu-id="02b11-133">Specifies the name of the server on which this cmdlet deletes the database.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02b11-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02b11-134">-Confirm</span></span>
<span data-ttu-id="02b11-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02b11-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b11-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02b11-136">-WhatIf</span></span>
<span data-ttu-id="02b11-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02b11-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02b11-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02b11-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b11-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b11-139">CommonParameters</span></span>
<span data-ttu-id="02b11-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02b11-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b11-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02b11-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b11-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02b11-142">INPUTS</span></span>

### <span data-ttu-id="02b11-143">Microsoft. WindowsAzure. kommandon. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="02b11-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="02b11-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02b11-144">OUTPUTS</span></span>

## <span data-ttu-id="02b11-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02b11-145">NOTES</span></span>
* <span data-ttu-id="02b11-146">På grund av åtgärdens allvar ber den här cmdleten dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="02b11-146">Because of the severity of the operation, by default, this cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="02b11-147">Ange parametern *Force* för att hoppa över bekräftelsen.</span><span class="sxs-lookup"><span data-stu-id="02b11-147">To skip confirmation, specify the *Force* parameter.</span></span>

## <span data-ttu-id="02b11-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02b11-148">RELATED LINKS</span></span>

[<span data-ttu-id="02b11-149">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="02b11-149">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="02b11-150">Ta bort databas</span><span class="sxs-lookup"><span data-stu-id="02b11-150">Delete Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[<span data-ttu-id="02b11-151">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="02b11-151">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="02b11-152">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="02b11-152">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="02b11-153">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="02b11-153">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="02b11-154">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="02b11-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="02b11-155">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="02b11-155">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


