---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: 4c71a5b71c04c8593443820989c935852b8a002b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577575"
---
# <span data-ttu-id="2de32-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="2de32-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="2de32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2de32-102">SYNOPSIS</span></span>
<span data-ttu-id="2de32-103">Definierar en anpassad princip för logg insamling.</span><span class="sxs-lookup"><span data-stu-id="2de32-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2de32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2de32-104">SYNTAX</span></span>

### <span data-ttu-id="2de32-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="2de32-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2de32-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2de32-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2de32-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2de32-107">DESCRIPTION</span></span>
<span data-ttu-id="2de32-108">Cmdleten **New-AzureRmOperationalInsightsCustomLogDataSource** definierar en anpassad policy för logg insamling.</span><span class="sxs-lookup"><span data-stu-id="2de32-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="2de32-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2de32-109">EXAMPLES</span></span>

## <span data-ttu-id="2de32-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2de32-110">PARAMETERS</span></span>

### <span data-ttu-id="2de32-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="2de32-111">-CustomLogRawJson</span></span>
<span data-ttu-id="2de32-112">Anger den anpassade samlings principen som en hexadecimal-sträng (RAW Java Script Object Notation).</span><span class="sxs-lookup"><span data-stu-id="2de32-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de32-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2de32-113">-Force</span></span>
<span data-ttu-id="2de32-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2de32-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2de32-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="2de32-115">-Name</span></span>
<span data-ttu-id="2de32-116">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="2de32-116">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de32-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de32-117">-ResourceGroupName</span></span>
<span data-ttu-id="2de32-118">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="2de32-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de32-119">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="2de32-119">-Workspace</span></span>
<span data-ttu-id="2de32-120">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2de32-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2de32-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2de32-121">-WorkspaceName</span></span>
<span data-ttu-id="2de32-122">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2de32-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de32-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2de32-123">-Confirm</span></span>
<span data-ttu-id="2de32-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2de32-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2de32-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de32-125">-WhatIf</span></span>
<span data-ttu-id="2de32-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2de32-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2de32-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2de32-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2de32-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de32-128">-DefaultProfile</span></span>
<span data-ttu-id="2de32-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2de32-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2de32-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de32-130">CommonParameters</span></span>
<span data-ttu-id="2de32-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de32-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de32-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de32-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de32-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2de32-133">INPUTS</span></span>

### <span data-ttu-id="2de32-134">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2de32-134">PSWorkspace</span></span>
<span data-ttu-id="2de32-135">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2de32-135">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="2de32-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2de32-136">OUTPUTS</span></span>

### <span data-ttu-id="2de32-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2de32-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2de32-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2de32-138">NOTES</span></span>

## <span data-ttu-id="2de32-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2de32-139">RELATED LINKS</span></span>

[<span data-ttu-id="2de32-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="2de32-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="2de32-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="2de32-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

