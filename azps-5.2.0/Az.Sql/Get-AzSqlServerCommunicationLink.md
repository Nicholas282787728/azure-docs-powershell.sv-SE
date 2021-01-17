---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406080"
---
# <span data-ttu-id="dce20-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="dce20-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="dce20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dce20-102">SYNOPSIS</span></span>
<span data-ttu-id="dce20-103">Hämtar kommunikations Länkar för elastiska databas transaktioner mellan databas servrar.</span><span class="sxs-lookup"><span data-stu-id="dce20-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="dce20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dce20-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dce20-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dce20-105">DESCRIPTION</span></span>
<span data-ttu-id="dce20-106">Cmdleten **Get-AzSqlServerCommunicationLink** hämtar länkar mellan servrar och servrar för elastiska databas transaktioner i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="dce20-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="dce20-107">Ange namnet på en länk till en server för att visa egenskaperna för länken.</span><span class="sxs-lookup"><span data-stu-id="dce20-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="dce20-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dce20-108">EXAMPLES</span></span>

### <span data-ttu-id="dce20-109">Exempel 1: Hämta alla kommunikations Länkar för en server</span><span class="sxs-lookup"><span data-stu-id="dce20-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="dce20-110">Det här kommandot får alla server-till-Server-kommunikations Länkar för Elastic Database Transactions för den server som heter ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="dce20-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="dce20-111">Exempel 2: Hämta en specifik kommunikations länk för en server</span><span class="sxs-lookup"><span data-stu-id="dce20-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="dce20-112">Det här kommandot hämtar länken mellan server och server med namnet Link01.</span><span class="sxs-lookup"><span data-stu-id="dce20-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="dce20-113">Exempel 3: Hämta alla kommunikations Länkar för en server med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="dce20-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="dce20-114">Det här kommandot får alla server-till-Server-kommunikations Länkar för elastiska databas transaktioner för servern med namnet ContosoServer17 som börjar med "Link".</span><span class="sxs-lookup"><span data-stu-id="dce20-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="dce20-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dce20-115">PARAMETERS</span></span>

### <span data-ttu-id="dce20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce20-116">-DefaultProfile</span></span>
<span data-ttu-id="dce20-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dce20-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dce20-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="dce20-118">-LinkName</span></span>
<span data-ttu-id="dce20-119">Anger namnet på den server kommunikation som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="dce20-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dce20-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce20-120">-ResourceGroupName</span></span>
<span data-ttu-id="dce20-121">Anger namnet på den resurs grupp som servern som anges av parametern *servername* tillhör.</span><span class="sxs-lookup"><span data-stu-id="dce20-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="dce20-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dce20-122">-ServerName</span></span>
<span data-ttu-id="dce20-123">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="dce20-123">Specifies the name of a server.</span></span>
<span data-ttu-id="dce20-124">Den här servern innehåller en kommunikations länk som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="dce20-124">This server contains a communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dce20-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dce20-125">-Confirm</span></span>
<span data-ttu-id="dce20-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dce20-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dce20-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce20-127">-WhatIf</span></span>
<span data-ttu-id="dce20-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dce20-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dce20-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dce20-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dce20-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce20-130">CommonParameters</span></span>
<span data-ttu-id="dce20-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce20-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce20-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dce20-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce20-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dce20-133">INPUTS</span></span>

### <span data-ttu-id="dce20-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dce20-134">System.String</span></span>

## <span data-ttu-id="dce20-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dce20-135">OUTPUTS</span></span>

### <span data-ttu-id="dce20-136">Microsoft. Azure. commands. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="dce20-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="dce20-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dce20-137">NOTES</span></span>
* <span data-ttu-id="dce20-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL</span><span class="sxs-lookup"><span data-stu-id="dce20-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="dce20-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dce20-139">RELATED LINKS</span></span>

[<span data-ttu-id="dce20-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="dce20-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="dce20-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="dce20-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="dce20-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="dce20-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
