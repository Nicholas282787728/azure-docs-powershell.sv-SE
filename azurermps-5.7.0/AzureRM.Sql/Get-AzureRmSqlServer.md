---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: a3af56ab78cd31dde30939901eaff12fff78ffa2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581951"
---
# <span data-ttu-id="3c55b-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3c55b-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="3c55b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c55b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c55b-103">Returnerar information om SQL-databas servrar.</span><span class="sxs-lookup"><span data-stu-id="3c55b-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c55b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c55b-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c55b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c55b-105">DESCRIPTION</span></span>
<span data-ttu-id="3c55b-106">Cmdleten **Get-AzureRmSqlServer** returnerar information om en eller flera Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="3c55b-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="3c55b-107">Ange namnet på en server för att visa information för endast den servern.</span><span class="sxs-lookup"><span data-stu-id="3c55b-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="3c55b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c55b-108">EXAMPLES</span></span>

### <span data-ttu-id="3c55b-109">Exempel 1: Hämta alla instanser av SQL Server kopplade till en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="3c55b-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="3c55b-110">Med det här kommandot får du information om alla de Azure SQL-databaser som tilldelats resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3c55b-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="3c55b-111">Exempel 2: få information om en Azure SQL Database-Server</span><span class="sxs-lookup"><span data-stu-id="3c55b-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="3c55b-112">Det här kommandot får information om Azure SQL-databasfilen med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="3c55b-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="3c55b-113">Exempel 3: Hämta alla instanser av SQL Server i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="3c55b-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server03.database.windows.net
```

<span data-ttu-id="3c55b-114">Med det här kommandot får du information om alla Azure SQL-databas servrar i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3c55b-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="3c55b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c55b-115">PARAMETERS</span></span>

### <span data-ttu-id="3c55b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c55b-116">-DefaultProfile</span></span>
<span data-ttu-id="3c55b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3c55b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c55b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c55b-118">-ResourceGroupName</span></span>
<span data-ttu-id="3c55b-119">Anger namnet på den resurs grupp som servrar är tilldelade till.</span><span class="sxs-lookup"><span data-stu-id="3c55b-119">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c55b-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3c55b-120">-ServerName</span></span>
<span data-ttu-id="3c55b-121">Anger namnet på den server som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="3c55b-121">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c55b-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3c55b-122">-Confirm</span></span>
<span data-ttu-id="3c55b-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3c55b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c55b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c55b-124">-WhatIf</span></span>
<span data-ttu-id="3c55b-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3c55b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c55b-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3c55b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c55b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c55b-127">CommonParameters</span></span>
<span data-ttu-id="3c55b-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c55b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c55b-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c55b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c55b-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c55b-130">INPUTS</span></span>

### <span data-ttu-id="3c55b-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="3c55b-131">None</span></span>
<span data-ttu-id="3c55b-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3c55b-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3c55b-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c55b-133">OUTPUTS</span></span>

### <span data-ttu-id="3c55b-134">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="3c55b-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="3c55b-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c55b-135">NOTES</span></span>

## <span data-ttu-id="3c55b-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c55b-136">RELATED LINKS</span></span>

[<span data-ttu-id="3c55b-137">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3c55b-137">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="3c55b-138">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3c55b-138">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="3c55b-139">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3c55b-139">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="3c55b-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="3c55b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


