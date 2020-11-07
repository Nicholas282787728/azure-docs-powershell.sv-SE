---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: a754ff33cba0bcf6324be0eb947b592b8fd4a622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756324"
---
# <span data-ttu-id="26ee2-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="26ee2-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="26ee2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="26ee2-103">Skapar en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="26ee2-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26ee2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26ee2-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26ee2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26ee2-105">DESCRIPTION</span></span>
<span data-ttu-id="26ee2-106">Cmdleten **New-AzureRmSqlServer** skapar en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="26ee2-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="26ee2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26ee2-107">EXAMPLES</span></span>

### <span data-ttu-id="26ee2-108">Exempel 1: skapa en ny Azure SQL-databasserver</span><span class="sxs-lookup"><span data-stu-id="26ee2-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="26ee2-109">Det här kommandot skapar en version av en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="26ee2-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="26ee2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26ee2-110">PARAMETERS</span></span>

### <span data-ttu-id="26ee2-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="26ee2-111">-AssignIdentity</span></span>
<span data-ttu-id="26ee2-112">Skapa och tilldela en Azure Active Directory-identitet för den här servern för användning med Key Management Services, till exempel Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="26ee2-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="26ee2-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="26ee2-113">-Location</span></span>
<span data-ttu-id="26ee2-114">Anger platsen för data centret där denna cmdlet skapar servern.</span><span class="sxs-lookup"><span data-stu-id="26ee2-114">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="26ee2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26ee2-115">-ResourceGroupName</span></span>
<span data-ttu-id="26ee2-116">Anger namnet på den resurs grupp som den här cmdleten tilldelar servern.</span><span class="sxs-lookup"><span data-stu-id="26ee2-116">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="26ee2-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="26ee2-117">-ServerName</span></span>
<span data-ttu-id="26ee2-118">Anger namnet på den nya servern.</span><span class="sxs-lookup"><span data-stu-id="26ee2-118">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="26ee2-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="26ee2-119">-ServerVersion</span></span>
<span data-ttu-id="26ee2-120">Anger versionen för den nya servern.</span><span class="sxs-lookup"><span data-stu-id="26ee2-120">Specifies the version of the new server.</span></span> <span data-ttu-id="26ee2-121">De acceptabla värdena för den här parametern är: 2,0 och 12,0.</span><span class="sxs-lookup"><span data-stu-id="26ee2-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="26ee2-122">Ange 2,0 för att skapa en version 11-Server eller 12,0 för att skapa en version 12-Server.</span><span class="sxs-lookup"><span data-stu-id="26ee2-122">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="26ee2-123">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="26ee2-123">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="26ee2-124">Anger Server administratörs uppgifter för den nya servern.</span><span class="sxs-lookup"><span data-stu-id="26ee2-124">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="26ee2-125">För att hämta ett **PSCredential** -objekt, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="26ee2-125">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="26ee2-126">Om du vill ha mer information skriver du `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="26ee2-126">For more information, type `Get-Help
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

### <span data-ttu-id="26ee2-127">-Taggar</span><span class="sxs-lookup"><span data-stu-id="26ee2-127">-Tags</span></span>
<span data-ttu-id="26ee2-128">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="26ee2-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="26ee2-129">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="26ee2-129">For example:</span></span>

<span data-ttu-id="26ee2-130">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="26ee2-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="26ee2-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="26ee2-131">-Confirm</span></span>
<span data-ttu-id="26ee2-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="26ee2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26ee2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26ee2-133">-WhatIf</span></span>
<span data-ttu-id="26ee2-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="26ee2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26ee2-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="26ee2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26ee2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26ee2-136">-DefaultProfile</span></span>
<span data-ttu-id="26ee2-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26ee2-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26ee2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26ee2-138">CommonParameters</span></span>
<span data-ttu-id="26ee2-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26ee2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26ee2-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26ee2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26ee2-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26ee2-141">INPUTS</span></span>

## <span data-ttu-id="26ee2-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26ee2-142">OUTPUTS</span></span>

### <span data-ttu-id="26ee2-143">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="26ee2-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="26ee2-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26ee2-144">NOTES</span></span>

## <span data-ttu-id="26ee2-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26ee2-145">RELATED LINKS</span></span>

[<span data-ttu-id="26ee2-146">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="26ee2-146">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="26ee2-147">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="26ee2-147">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="26ee2-148">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="26ee2-148">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="26ee2-149">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="26ee2-149">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="26ee2-150">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="26ee2-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)