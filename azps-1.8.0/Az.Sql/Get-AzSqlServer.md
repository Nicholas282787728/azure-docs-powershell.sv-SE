---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: fb8769dcd8f989ad0715a799ce397eb0fe594126
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746684"
---
# <span data-ttu-id="1f23d-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1f23d-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="1f23d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f23d-102">SYNOPSIS</span></span>
<span data-ttu-id="1f23d-103">Returnerar information om SQL-databas servrar.</span><span class="sxs-lookup"><span data-stu-id="1f23d-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="1f23d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f23d-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f23d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f23d-105">DESCRIPTION</span></span>
<span data-ttu-id="1f23d-106">Cmdleten **Get-AzSqlServer** returnerar information om en eller flera Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="1f23d-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="1f23d-107">Ange namnet på en server för att visa information för endast den servern.</span><span class="sxs-lookup"><span data-stu-id="1f23d-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="1f23d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f23d-108">EXAMPLES</span></span>

### <span data-ttu-id="1f23d-109">Exempel 1: Hämta alla instanser av SQL Server kopplade till en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="1f23d-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="1f23d-110">Med det här kommandot får du information om alla de Azure SQL-databaser som tilldelats resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="1f23d-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="1f23d-111">Exempel 2: få information om en Azure SQL Database-Server</span><span class="sxs-lookup"><span data-stu-id="1f23d-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="1f23d-112">Det här kommandot får information om Azure SQL-databasfilen med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="1f23d-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="1f23d-113">Exempel 3: Hämta alla instanser av SQL Server i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="1f23d-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzSqlServer
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

<span data-ttu-id="1f23d-114">Med det här kommandot får du information om alla Azure SQL-databas servrar i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1f23d-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="1f23d-115">Exempel 4: Hämta alla instanser av SQL Server kopplade till en resurs grupp med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="1f23d-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "server*"
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

<span data-ttu-id="1f23d-116">Med det här kommandot får du information om alla de Azure SQL-databaser som tilldelats till resurs gruppen ResourceGroup01 som börjar med "Server".</span><span class="sxs-lookup"><span data-stu-id="1f23d-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="1f23d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f23d-117">PARAMETERS</span></span>

### <span data-ttu-id="1f23d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f23d-118">-DefaultProfile</span></span>
<span data-ttu-id="1f23d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1f23d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f23d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f23d-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f23d-121">Anger namnet på den resurs grupp som servrar är tilldelade till.</span><span class="sxs-lookup"><span data-stu-id="1f23d-121">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1f23d-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1f23d-122">-ServerName</span></span>
<span data-ttu-id="1f23d-123">Anger namnet på den server som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="1f23d-123">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1f23d-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f23d-124">-Confirm</span></span>
<span data-ttu-id="1f23d-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f23d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f23d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f23d-126">-WhatIf</span></span>
<span data-ttu-id="1f23d-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f23d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f23d-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f23d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f23d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f23d-129">CommonParameters</span></span>
<span data-ttu-id="1f23d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f23d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f23d-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f23d-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f23d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f23d-132">INPUTS</span></span>

### <span data-ttu-id="1f23d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1f23d-133">System.String</span></span>

## <span data-ttu-id="1f23d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f23d-134">OUTPUTS</span></span>

### <span data-ttu-id="1f23d-135">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1f23d-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="1f23d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f23d-136">NOTES</span></span>

## <span data-ttu-id="1f23d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f23d-137">RELATED LINKS</span></span>

[<span data-ttu-id="1f23d-138">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1f23d-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="1f23d-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1f23d-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="1f23d-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="1f23d-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="1f23d-141">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="1f23d-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


