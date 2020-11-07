---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: c9e3f55940f77d4627f4e3e4f7e9a26f47606206
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746564"
---
# <span data-ttu-id="fffcf-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="fffcf-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="fffcf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fffcf-102">SYNOPSIS</span></span>
<span data-ttu-id="fffcf-103">Tar bort en kommunikations länk för elastiska databas transaktioner mellan två servrar.</span><span class="sxs-lookup"><span data-stu-id="fffcf-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="fffcf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fffcf-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fffcf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fffcf-105">DESCRIPTION</span></span>
<span data-ttu-id="fffcf-106">Cmdleten **Remove-AzSqlServerCommunicationLink** tar bort en länk för en server-till-server-kommunikation för elastiska databas transaktioner i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="fffcf-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="fffcf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fffcf-107">EXAMPLES</span></span>

### <span data-ttu-id="fffcf-108">Exempel 1: ta bort en kommunikations länk</span><span class="sxs-lookup"><span data-stu-id="fffcf-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="fffcf-109">Det här kommandot tar bort en länk för server-till-server-kommunikation med namnet Link01 på ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="fffcf-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="fffcf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fffcf-110">PARAMETERS</span></span>

### <span data-ttu-id="fffcf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fffcf-111">-DefaultProfile</span></span>
<span data-ttu-id="fffcf-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fffcf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fffcf-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fffcf-113">-Force</span></span>
<span data-ttu-id="fffcf-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="fffcf-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fffcf-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="fffcf-115">-LinkName</span></span>
<span data-ttu-id="fffcf-116">Anger namnet på den server kommunikation som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="fffcf-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fffcf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fffcf-117">-ResourceGroupName</span></span>
<span data-ttu-id="fffcf-118">Anger namnet på den resurs grupp som servern som anges av parametern *servername* tillhör.</span><span class="sxs-lookup"><span data-stu-id="fffcf-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="fffcf-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fffcf-119">-ServerName</span></span>
<span data-ttu-id="fffcf-120">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="fffcf-120">Specifies the name of a server.</span></span>
<span data-ttu-id="fffcf-121">Den här servern innehåller den kommunikations länk som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fffcf-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="fffcf-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fffcf-122">-Confirm</span></span>
<span data-ttu-id="fffcf-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fffcf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fffcf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fffcf-124">-WhatIf</span></span>
<span data-ttu-id="fffcf-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fffcf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fffcf-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fffcf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fffcf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fffcf-127">CommonParameters</span></span>
<span data-ttu-id="fffcf-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fffcf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fffcf-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fffcf-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fffcf-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fffcf-130">INPUTS</span></span>

### <span data-ttu-id="fffcf-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fffcf-131">System.String</span></span>

## <span data-ttu-id="fffcf-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fffcf-132">OUTPUTS</span></span>

### <span data-ttu-id="fffcf-133">Microsoft. Azure. commands. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="fffcf-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="fffcf-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fffcf-134">NOTES</span></span>
* <span data-ttu-id="fffcf-135">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL</span><span class="sxs-lookup"><span data-stu-id="fffcf-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="fffcf-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fffcf-136">RELATED LINKS</span></span>

[<span data-ttu-id="fffcf-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="fffcf-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="fffcf-138">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="fffcf-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="fffcf-139">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="fffcf-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
