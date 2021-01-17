---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396171"
---
# <span data-ttu-id="94906-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="94906-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="94906-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94906-102">SYNOPSIS</span></span>
<span data-ttu-id="94906-103">Återställa en borttagen arbets yta.</span><span class="sxs-lookup"><span data-stu-id="94906-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="94906-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94906-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94906-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94906-105">DESCRIPTION</span></span>
<span data-ttu-id="94906-106">Återställa en borttagen arbets yta.</span><span class="sxs-lookup"><span data-stu-id="94906-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="94906-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94906-107">EXAMPLES</span></span>

### <span data-ttu-id="94906-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="94906-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="94906-109">Återställ borttagen arbets yta.</span><span class="sxs-lookup"><span data-stu-id="94906-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="94906-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94906-110">PARAMETERS</span></span>

### <span data-ttu-id="94906-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94906-111">-DefaultProfile</span></span>
<span data-ttu-id="94906-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94906-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94906-113">-Force</span><span class="sxs-lookup"><span data-stu-id="94906-113">-Force</span></span>
<span data-ttu-id="94906-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="94906-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="94906-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="94906-115">-Location</span></span>
<span data-ttu-id="94906-116">Den geografiska region som arbets ytan ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="94906-116">The geographic region that the workspace will be created in.</span></span>

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

### <span data-ttu-id="94906-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="94906-117">-Name</span></span>
<span data-ttu-id="94906-118">Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="94906-118">The workspace name.</span></span>

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

### <span data-ttu-id="94906-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94906-119">-ResourceGroupName</span></span>
<span data-ttu-id="94906-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="94906-120">The resource group name.</span></span>

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

### <span data-ttu-id="94906-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94906-121">-Confirm</span></span>
<span data-ttu-id="94906-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94906-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94906-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94906-123">-WhatIf</span></span>
<span data-ttu-id="94906-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94906-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94906-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94906-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94906-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94906-126">CommonParameters</span></span>
<span data-ttu-id="94906-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94906-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94906-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94906-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94906-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94906-129">INPUTS</span></span>

### <span data-ttu-id="94906-130">System. String</span><span class="sxs-lookup"><span data-stu-id="94906-130">System.String</span></span>

## <span data-ttu-id="94906-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94906-131">OUTPUTS</span></span>

### <span data-ttu-id="94906-132">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="94906-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="94906-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94906-133">NOTES</span></span>

## <span data-ttu-id="94906-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94906-134">RELATED LINKS</span></span>
