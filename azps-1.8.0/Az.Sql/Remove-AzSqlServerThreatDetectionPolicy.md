---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5b75c2058fb7a6ddf323ebeaa6aad6967dcb5b01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746550"
---
# <span data-ttu-id="9b764-101">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9b764-101">Remove-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="9b764-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b764-102">SYNOPSIS</span></span>
<span data-ttu-id="9b764-103">Tar bort hot identifierings policyn från en server.</span><span class="sxs-lookup"><span data-stu-id="9b764-103">Removes the threat detection policy from a server.</span></span>

## <span data-ttu-id="9b764-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b764-104">SYNTAX</span></span>

```
Remove-AzSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b764-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b764-105">DESCRIPTION</span></span>
<span data-ttu-id="9b764-106">Remove-AzSqlServerThreatDetectionPolicy cmdlet tar bort hot Detection policyn från en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9b764-106">The Remove-AzSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>
<span data-ttu-id="9b764-107">Om du vill använda den här cmdleten anger du parametrarna ResourceGroupName och ServerName för att identifiera den server som cmdleten tar bort från.</span><span class="sxs-lookup"><span data-stu-id="9b764-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="9b764-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b764-108">EXAMPLES</span></span>

### <span data-ttu-id="9b764-109">Exempel 1: ta bort en princip för hot identifiering för en databas</span><span class="sxs-lookup"><span data-stu-id="9b764-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\> Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="9b764-110">Det här kommandot tar bort hot identifierings policyn från en server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="9b764-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="9b764-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b764-111">PARAMETERS</span></span>

### <span data-ttu-id="9b764-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b764-112">-DefaultProfile</span></span>
<span data-ttu-id="9b764-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9b764-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b764-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b764-114">-PassThru</span></span>
<span data-ttu-id="9b764-115">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="9b764-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9b764-116">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9b764-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9b764-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b764-117">-ResourceGroupName</span></span>
<span data-ttu-id="9b764-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="9b764-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="9b764-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9b764-119">-ServerName</span></span>
<span data-ttu-id="9b764-120">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="9b764-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b764-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b764-121">-Confirm</span></span>
<span data-ttu-id="9b764-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b764-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b764-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b764-123">-WhatIf</span></span>
<span data-ttu-id="9b764-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b764-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b764-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b764-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b764-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b764-126">CommonParameters</span></span>
<span data-ttu-id="9b764-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b764-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b764-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b764-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b764-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b764-129">INPUTS</span></span>

### <span data-ttu-id="9b764-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9b764-130">System.String</span></span>

## <span data-ttu-id="9b764-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b764-131">OUTPUTS</span></span>

### <span data-ttu-id="9b764-132">Microsoft. Azure. commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9b764-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="9b764-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b764-133">NOTES</span></span>

## <span data-ttu-id="9b764-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b764-134">RELATED LINKS</span></span>

[<span data-ttu-id="9b764-135">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="9b764-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

