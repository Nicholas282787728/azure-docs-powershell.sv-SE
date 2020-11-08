---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: ec2e71e6556824ad92e1a5839f0b10c91960fec0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101871"
---
# <span data-ttu-id="4179c-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="4179c-101">New-AzSqlServer</span></span>

## <span data-ttu-id="4179c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4179c-102">SYNOPSIS</span></span>
<span data-ttu-id="4179c-103">Skapar en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="4179c-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="4179c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4179c-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4179c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4179c-105">DESCRIPTION</span></span>
<span data-ttu-id="4179c-106">Cmdleten **New-AzSqlServer** skapar en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="4179c-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="4179c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4179c-107">EXAMPLES</span></span>

### <span data-ttu-id="4179c-108">Exempel 1: skapa en ny Azure SQL-databasserver</span><span class="sxs-lookup"><span data-stu-id="4179c-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="4179c-109">Det här kommandot skapar en version av en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="4179c-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="4179c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4179c-110">PARAMETERS</span></span>

### <span data-ttu-id="4179c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4179c-111">-AsJob</span></span>
<span data-ttu-id="4179c-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4179c-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4179c-113">-AssignIdentity</span></span>
<span data-ttu-id="4179c-114">Skapa och tilldela en Azure Active Directory-identitet för den här servern för användning med Key Management Services, till exempel Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="4179c-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4179c-115">-DefaultProfile</span></span>
<span data-ttu-id="4179c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4179c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="4179c-117">-Location</span></span>
<span data-ttu-id="4179c-118">Anger platsen för data centret där denna cmdlet skapar servern.</span><span class="sxs-lookup"><span data-stu-id="4179c-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4179c-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="4179c-120">Den minsta TLS-version som ska tillämpas för SQL Server</span><span class="sxs-lookup"><span data-stu-id="4179c-120">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="4179c-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="4179c-122">Tar en flagga som är aktive rad eller inaktiv för att ange om offentliga nätverks åtkomst till servern tillåts eller inte.</span><span class="sxs-lookup"><span data-stu-id="4179c-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="4179c-123">När det är inaktiverat kan bara anslutningar som görs med privata länkar nå den här servern.</span><span class="sxs-lookup"><span data-stu-id="4179c-123">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4179c-124">-ResourceGroupName</span></span>
<span data-ttu-id="4179c-125">Anger namnet på den resurs grupp som den här cmdleten tilldelar servern.</span><span class="sxs-lookup"><span data-stu-id="4179c-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4179c-126">-ServerName</span></span>
<span data-ttu-id="4179c-127">Anger namnet på den nya servern.</span><span class="sxs-lookup"><span data-stu-id="4179c-127">Specifies the name of the new server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="4179c-128">-ServerVersion</span></span>
<span data-ttu-id="4179c-129">Anger versionen för den nya servern.</span><span class="sxs-lookup"><span data-stu-id="4179c-129">Specifies the version of the new server.</span></span> <span data-ttu-id="4179c-130">De acceptabla värdena för den här parametern är: 2,0 och 12,0.</span><span class="sxs-lookup"><span data-stu-id="4179c-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="4179c-131">Ange 2,0 för att skapa en version 11-Server eller 12,0 för att skapa en version 12-Server.</span><span class="sxs-lookup"><span data-stu-id="4179c-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-132">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="4179c-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="4179c-133">Anger Server administratörs uppgifter för den nya servern.</span><span class="sxs-lookup"><span data-stu-id="4179c-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="4179c-134">För att hämta ett **PSCredential** -objekt, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="4179c-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="4179c-135">Om du vill ha mer information skriver du `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="4179c-135">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-136">-Taggar</span><span class="sxs-lookup"><span data-stu-id="4179c-136">-Tags</span></span>
<span data-ttu-id="4179c-137">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4179c-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4179c-138">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="4179c-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4179c-139">-Confirm</span></span>
<span data-ttu-id="4179c-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4179c-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4179c-141">-WhatIf</span></span>
<span data-ttu-id="4179c-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4179c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4179c-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4179c-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4179c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4179c-144">CommonParameters</span></span>
<span data-ttu-id="4179c-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4179c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4179c-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4179c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4179c-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4179c-147">INPUTS</span></span>

### <span data-ttu-id="4179c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4179c-148">System.String</span></span>

## <span data-ttu-id="4179c-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4179c-149">OUTPUTS</span></span>

### <span data-ttu-id="4179c-150">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="4179c-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="4179c-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4179c-151">NOTES</span></span>

## <span data-ttu-id="4179c-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4179c-152">RELATED LINKS</span></span>

[<span data-ttu-id="4179c-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="4179c-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="4179c-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="4179c-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="4179c-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="4179c-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="4179c-156">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4179c-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="4179c-157">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="4179c-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
