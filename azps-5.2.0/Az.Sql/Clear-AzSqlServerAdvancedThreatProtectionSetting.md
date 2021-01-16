---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394328"
---
# <span data-ttu-id="03dcf-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="03dcf-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="03dcf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="03dcf-103">Tar bort de avancerade skydds inställningarna från en server.</span><span class="sxs-lookup"><span data-stu-id="03dcf-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="03dcf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03dcf-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03dcf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03dcf-105">DESCRIPTION</span></span>
<span data-ttu-id="03dcf-106">Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet tar bort avancerade inställningar för skydd mot en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="03dcf-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="03dcf-107">Använd den här cmdleten genom att ange parametrarna ResourceGroupName och ServerName för att identifiera den server som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="03dcf-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="03dcf-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03dcf-108">EXAMPLES</span></span>

### <span data-ttu-id="03dcf-109">Exempel 1: ta bort avancerade skydds inställningar för en databas</span><span class="sxs-lookup"><span data-stu-id="03dcf-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="03dcf-110">Det här kommandot tar bort de avancerade skydds inställningarna från en server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="03dcf-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="03dcf-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03dcf-111">PARAMETERS</span></span>

### <span data-ttu-id="03dcf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03dcf-112">-DefaultProfile</span></span>
<span data-ttu-id="03dcf-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="03dcf-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03dcf-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03dcf-114">-PassThru</span></span>
<span data-ttu-id="03dcf-115">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="03dcf-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03dcf-116">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="03dcf-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03dcf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03dcf-117">-ResourceGroupName</span></span>
<span data-ttu-id="03dcf-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="03dcf-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="03dcf-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="03dcf-119">-ServerName</span></span>
<span data-ttu-id="03dcf-120">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="03dcf-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="03dcf-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="03dcf-121">-Confirm</span></span>
<span data-ttu-id="03dcf-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="03dcf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03dcf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03dcf-123">-WhatIf</span></span>
<span data-ttu-id="03dcf-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="03dcf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03dcf-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="03dcf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03dcf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03dcf-126">CommonParameters</span></span>
<span data-ttu-id="03dcf-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03dcf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03dcf-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03dcf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03dcf-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03dcf-129">INPUTS</span></span>

### <span data-ttu-id="03dcf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="03dcf-130">System.String</span></span>

## <span data-ttu-id="03dcf-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03dcf-131">OUTPUTS</span></span>

### <span data-ttu-id="03dcf-132">Microsoft. Azure. commands. SQL. ThreatDetection. Model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="03dcf-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="03dcf-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03dcf-133">NOTES</span></span>

## <span data-ttu-id="03dcf-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03dcf-134">RELATED LINKS</span></span>

[<span data-ttu-id="03dcf-135">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="03dcf-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

