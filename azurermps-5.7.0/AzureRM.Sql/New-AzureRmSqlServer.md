---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: 6b9fa4c7fff426f9af19484c7576b9dee341a82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756060"
---
# <span data-ttu-id="61bc3-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="61bc3-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="61bc3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="61bc3-103">Skapar en SQL-databasserver.</span><span class="sxs-lookup"><span data-stu-id="61bc3-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61bc3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61bc3-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61bc3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61bc3-105">DESCRIPTION</span></span>
<span data-ttu-id="61bc3-106">Cmdleten **New-AzureRmSqlServer** skapar en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="61bc3-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="61bc3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61bc3-107">EXAMPLES</span></span>

### <span data-ttu-id="61bc3-108">Exempel 1: skapa en ny Azure SQL-databasserver</span><span class="sxs-lookup"><span data-stu-id="61bc3-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="61bc3-109">Det här kommandot skapar en version av en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="61bc3-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="61bc3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61bc3-110">PARAMETERS</span></span>

### <span data-ttu-id="61bc3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61bc3-111">-AsJob</span></span>
<span data-ttu-id="61bc3-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="61bc3-112">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="61bc3-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="61bc3-113">-AssignIdentity</span></span>
<span data-ttu-id="61bc3-114">Skapa och tilldela en Azure Active Directory-identitet för den här servern för användning med Key Management Services, till exempel Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="61bc3-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="61bc3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61bc3-115">-DefaultProfile</span></span>
<span data-ttu-id="61bc3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="61bc3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bc3-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="61bc3-117">-Location</span></span>
<span data-ttu-id="61bc3-118">Anger platsen för data centret där denna cmdlet skapar servern.</span><span class="sxs-lookup"><span data-stu-id="61bc3-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bc3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61bc3-119">-ResourceGroupName</span></span>
<span data-ttu-id="61bc3-120">Anger namnet på den resurs grupp som den här cmdleten tilldelar servern.</span><span class="sxs-lookup"><span data-stu-id="61bc3-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61bc3-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="61bc3-121">-ServerName</span></span>
<span data-ttu-id="61bc3-122">Anger namnet på den nya servern.</span><span class="sxs-lookup"><span data-stu-id="61bc3-122">Specifies the name of the new server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bc3-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="61bc3-123">-ServerVersion</span></span>
<span data-ttu-id="61bc3-124">Anger versionen för den nya servern.</span><span class="sxs-lookup"><span data-stu-id="61bc3-124">Specifies the version of the new server.</span></span> <span data-ttu-id="61bc3-125">De acceptabla värdena för den här parametern är: 2,0 och 12,0.</span><span class="sxs-lookup"><span data-stu-id="61bc3-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="61bc3-126">Ange 2,0 för att skapa en version 11-Server eller 12,0 för att skapa en version 12-Server.</span><span class="sxs-lookup"><span data-stu-id="61bc3-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bc3-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="61bc3-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="61bc3-128">Anger Server administratörs uppgifter för den nya servern.</span><span class="sxs-lookup"><span data-stu-id="61bc3-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="61bc3-129">För att hämta ett **PSCredential** -objekt, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="61bc3-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="61bc3-130">Om du vill ha mer information skriver du `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="61bc3-130">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bc3-131">-Taggar</span><span class="sxs-lookup"><span data-stu-id="61bc3-131">-Tags</span></span>
<span data-ttu-id="61bc3-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="61bc3-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="61bc3-133">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="61bc3-133">For example:</span></span>

<span data-ttu-id="61bc3-134">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="61bc3-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bc3-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="61bc3-135">-Confirm</span></span>
<span data-ttu-id="61bc3-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="61bc3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61bc3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61bc3-137">-WhatIf</span></span>
<span data-ttu-id="61bc3-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="61bc3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61bc3-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="61bc3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61bc3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bc3-140">CommonParameters</span></span>
<span data-ttu-id="61bc3-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61bc3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bc3-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61bc3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bc3-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61bc3-143">INPUTS</span></span>

### <span data-ttu-id="61bc3-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="61bc3-144">None</span></span>
<span data-ttu-id="61bc3-145">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="61bc3-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61bc3-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61bc3-146">OUTPUTS</span></span>

### <span data-ttu-id="61bc3-147">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="61bc3-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="61bc3-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61bc3-148">NOTES</span></span>

## <span data-ttu-id="61bc3-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61bc3-149">RELATED LINKS</span></span>

[<span data-ttu-id="61bc3-150">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="61bc3-150">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="61bc3-151">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="61bc3-151">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="61bc3-152">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="61bc3-152">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="61bc3-153">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="61bc3-153">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="61bc3-154">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="61bc3-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
