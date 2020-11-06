---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: f2d687ce10edf56fc424c03873c733971f70e546
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582171"
---
# <span data-ttu-id="b5831-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b5831-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="b5831-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5831-102">SYNOPSIS</span></span>
<span data-ttu-id="b5831-103">Returnerar information om SQL-databas servrar.</span><span class="sxs-lookup"><span data-stu-id="b5831-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5831-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5831-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5831-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5831-105">DESCRIPTION</span></span>
<span data-ttu-id="b5831-106">Cmdleten **Get-AzureRmSqlServer** returnerar information om en eller flera Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="b5831-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="b5831-107">Ange namnet på en server för att visa information för endast den servern.</span><span class="sxs-lookup"><span data-stu-id="b5831-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="b5831-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5831-108">EXAMPLES</span></span>

### <span data-ttu-id="b5831-109">Exempel 1: Hämta alla instanser av SQL Server kopplade till en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="b5831-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLoginSqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="b5831-110">Med det här kommandot får du information om alla de Azure SQL-databaser som tilldelats resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b5831-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="b5831-111">Exempel 2: få information om en Azure SQL Database-Server</span><span class="sxs-lookup"><span data-stu-id="b5831-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="b5831-112">Det här kommandot får information om Azure SQL-databasfilen med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="b5831-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="b5831-113">Exempel 3: Hämta alla instanser av SQL Server i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="b5831-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="b5831-114">Med det här kommandot får du information om alla Azure SQL-databas servrar i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b5831-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="b5831-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5831-115">PARAMETERS</span></span>

### <span data-ttu-id="b5831-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5831-116">-ResourceGroupName</span></span>
<span data-ttu-id="b5831-117">Anger namnet på den resurs grupp som servrar är tilldelade till.</span><span class="sxs-lookup"><span data-stu-id="b5831-117">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5831-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b5831-118">-ServerName</span></span>
<span data-ttu-id="b5831-119">Anger namnet på den server som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="b5831-119">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5831-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5831-120">-Confirm</span></span>
<span data-ttu-id="b5831-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5831-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5831-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5831-122">-WhatIf</span></span>
<span data-ttu-id="b5831-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5831-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5831-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5831-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5831-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5831-125">-DefaultProfile</span></span>
<span data-ttu-id="b5831-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5831-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5831-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5831-127">CommonParameters</span></span>
<span data-ttu-id="b5831-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5831-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5831-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5831-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5831-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5831-130">INPUTS</span></span>

## <span data-ttu-id="b5831-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5831-131">OUTPUTS</span></span>

### <span data-ttu-id="b5831-132">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b5831-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="b5831-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5831-133">NOTES</span></span>

## <span data-ttu-id="b5831-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5831-134">RELATED LINKS</span></span>

[<span data-ttu-id="b5831-135">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b5831-135">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="b5831-136">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b5831-136">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="b5831-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="b5831-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="b5831-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="b5831-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


