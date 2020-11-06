---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 3d53227f3d339419cfab5656de42fa52abb3bf08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579928"
---
# <span data-ttu-id="48073-101">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="48073-101">Get-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="48073-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48073-102">SYNOPSIS</span></span>
<span data-ttu-id="48073-103">Hämtar kommunikations Länkar för elastiska databas transaktioner mellan databas servrar.</span><span class="sxs-lookup"><span data-stu-id="48073-103">Gets communication links for elastic database transactions between database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48073-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48073-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48073-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48073-105">DESCRIPTION</span></span>
<span data-ttu-id="48073-106">Cmdleten **Get-AzureRmSqlServerCommunicationLink** hämtar länkar mellan servrar och servrar för elastiska databas transaktioner i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="48073-106">The **Get-AzureRmSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="48073-107">Ange namnet på en länk till en server för att visa egenskaperna för länken.</span><span class="sxs-lookup"><span data-stu-id="48073-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="48073-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48073-108">EXAMPLES</span></span>

### <span data-ttu-id="48073-109">Exempel 1: Hämta alla kommunikations Länkar för en server</span><span class="sxs-lookup"><span data-stu-id="48073-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="48073-110">Det här kommandot får alla server-till-Server-kommunikations Länkar för Elastic Database Transactions för den server som heter ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="48073-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="48073-111">Exempel 2: Hämta en specifik kommunikations länk för en server</span><span class="sxs-lookup"><span data-stu-id="48073-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="48073-112">Det här kommandot hämtar länken mellan server och server med namnet Link01.</span><span class="sxs-lookup"><span data-stu-id="48073-112">This command gets the server-to-server communication link named Link01.</span></span>

## <span data-ttu-id="48073-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48073-113">PARAMETERS</span></span>

### <span data-ttu-id="48073-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48073-114">-DefaultProfile</span></span>
<span data-ttu-id="48073-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="48073-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48073-116">-LinkName</span><span class="sxs-lookup"><span data-stu-id="48073-116">-LinkName</span></span>
<span data-ttu-id="48073-117">Anger namnet på den server kommunikation som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="48073-117">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="48073-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48073-118">-ResourceGroupName</span></span>
<span data-ttu-id="48073-119">Anger namnet på den resurs grupp som servern som anges av parametern *servername* tillhör.</span><span class="sxs-lookup"><span data-stu-id="48073-119">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="48073-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="48073-120">-ServerName</span></span>
<span data-ttu-id="48073-121">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="48073-121">Specifies the name of a server.</span></span>
<span data-ttu-id="48073-122">Den här servern innehåller en kommunikations länk som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="48073-122">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="48073-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48073-123">-Confirm</span></span>
<span data-ttu-id="48073-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48073-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48073-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48073-125">-WhatIf</span></span>
<span data-ttu-id="48073-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="48073-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48073-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="48073-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48073-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48073-128">CommonParameters</span></span>
<span data-ttu-id="48073-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48073-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48073-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48073-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48073-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48073-131">INPUTS</span></span>

### <span data-ttu-id="48073-132">System. String</span><span class="sxs-lookup"><span data-stu-id="48073-132">System.String</span></span>

## <span data-ttu-id="48073-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48073-133">OUTPUTS</span></span>

### <span data-ttu-id="48073-134">Microsoft. Azure. commands. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="48073-134">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="48073-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48073-135">NOTES</span></span>
* <span data-ttu-id="48073-136">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL</span><span class="sxs-lookup"><span data-stu-id="48073-136">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="48073-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48073-137">RELATED LINKS</span></span>

[<span data-ttu-id="48073-138">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="48073-138">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="48073-139">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="48073-139">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="48073-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="48073-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
