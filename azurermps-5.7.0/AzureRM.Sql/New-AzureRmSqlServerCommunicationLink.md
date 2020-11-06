---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 0492b81e5674ea08ad98dff1fca75335b1ec8fa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579316"
---
# <span data-ttu-id="75dd7-101">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="75dd7-101">New-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="75dd7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="75dd7-103">Skapar en kommunikations länk för elastiska databas transaktioner mellan två SQL-databas servrar.</span><span class="sxs-lookup"><span data-stu-id="75dd7-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75dd7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75dd7-104">SYNTAX</span></span>

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75dd7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75dd7-105">DESCRIPTION</span></span>
<span data-ttu-id="75dd7-106">Cmdleten **New-AzureRmSqlServerCommunicationLink** skapar en kommunikations länk för elastiska databas transaktioner mellan två logiska servrar i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="75dd7-106">The **New-AzureRmSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="75dd7-107">Transaktioner i elastiska databaser kan spänna över databaser på någon av de Parada servrarna.</span><span class="sxs-lookup"><span data-stu-id="75dd7-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="75dd7-108">Du kan skapa mer än en länk på en server.</span><span class="sxs-lookup"><span data-stu-id="75dd7-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="75dd7-109">Därför kan elastiska databas transaktioner sträcka sig över ett större antal servrar.</span><span class="sxs-lookup"><span data-stu-id="75dd7-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="75dd7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75dd7-110">EXAMPLES</span></span>

### <span data-ttu-id="75dd7-111">Exempel 1: skapa en kommunikations länk</span><span class="sxs-lookup"><span data-stu-id="75dd7-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="75dd7-112">Det här kommandot skapar en länk som heter Link01 mellan ContosoServer17 och ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="75dd7-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="75dd7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75dd7-113">PARAMETERS</span></span>

### <span data-ttu-id="75dd7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75dd7-114">-AsJob</span></span>
<span data-ttu-id="75dd7-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="75dd7-115">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="75dd7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75dd7-116">-DefaultProfile</span></span>
<span data-ttu-id="75dd7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="75dd7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75dd7-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="75dd7-118">-LinkName</span></span>
<span data-ttu-id="75dd7-119">Anger namnet på den server kommunikation som skapas av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75dd7-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="75dd7-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="75dd7-120">-PartnerServer</span></span>
<span data-ttu-id="75dd7-121">Anger namnet på den andra servern som ska ingå i den här kommunikations länken.</span><span class="sxs-lookup"><span data-stu-id="75dd7-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="75dd7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75dd7-122">-ResourceGroupName</span></span>
<span data-ttu-id="75dd7-123">Anger namnet på den resurs grupp som servern som anges av parametern *servername* tillhör.</span><span class="sxs-lookup"><span data-stu-id="75dd7-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="75dd7-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="75dd7-124">-ServerName</span></span>
<span data-ttu-id="75dd7-125">Anger namnet på den server där denna cmdlet ställer in kommunikations länken.</span><span class="sxs-lookup"><span data-stu-id="75dd7-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75dd7-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75dd7-126">-Confirm</span></span>
<span data-ttu-id="75dd7-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75dd7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75dd7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75dd7-128">-WhatIf</span></span>
<span data-ttu-id="75dd7-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75dd7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75dd7-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75dd7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75dd7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75dd7-131">CommonParameters</span></span>
<span data-ttu-id="75dd7-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75dd7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75dd7-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75dd7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75dd7-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75dd7-134">INPUTS</span></span>

### <span data-ttu-id="75dd7-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="75dd7-135">None</span></span>
<span data-ttu-id="75dd7-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="75dd7-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75dd7-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75dd7-137">OUTPUTS</span></span>

### <span data-ttu-id="75dd7-138">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="75dd7-138">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="75dd7-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75dd7-139">NOTES</span></span>
* <span data-ttu-id="75dd7-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL</span><span class="sxs-lookup"><span data-stu-id="75dd7-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="75dd7-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75dd7-141">RELATED LINKS</span></span>

[<span data-ttu-id="75dd7-142">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="75dd7-142">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="75dd7-143">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="75dd7-143">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="75dd7-144">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="75dd7-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
