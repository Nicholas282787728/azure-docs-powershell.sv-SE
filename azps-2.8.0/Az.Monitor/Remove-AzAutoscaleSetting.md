---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAutoscaleSetting.md
ms.openlocfilehash: 21cc1e70e0122e21dac5cb78cfa4f4346cf72e5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918900"
---
# <span data-ttu-id="8ba98-101">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8ba98-101">Remove-AzAutoscaleSetting</span></span>

## <span data-ttu-id="8ba98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ba98-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba98-103">Tar bort en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="8ba98-103">Removes an Autoscale setting.</span></span>

## <span data-ttu-id="8ba98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ba98-104">SYNTAX</span></span>

```
Remove-AzAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ba98-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ba98-105">DESCRIPTION</span></span>
<span data-ttu-id="8ba98-106">Cmdleten **Remove-AzAutoscaleSetting** tar bort en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="8ba98-106">The **Remove-AzAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="8ba98-107">Du måste ange namnet på inställningen och namnet på resurs gruppen som den har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="8ba98-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="8ba98-108">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="8ba98-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="8ba98-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ba98-109">EXAMPLES</span></span>

## <span data-ttu-id="8ba98-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ba98-110">PARAMETERS</span></span>

### <span data-ttu-id="8ba98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba98-111">-DefaultProfile</span></span>
<span data-ttu-id="8ba98-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8ba98-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ba98-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="8ba98-113">-Name</span></span>
<span data-ttu-id="8ba98-114">Anger namnet på den autoskalningsinställning som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8ba98-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="8ba98-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba98-115">-ResourceGroupName</span></span>
<span data-ttu-id="8ba98-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8ba98-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba98-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8ba98-117">-Confirm</span></span>
<span data-ttu-id="8ba98-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8ba98-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ba98-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba98-119">-WhatIf</span></span>
<span data-ttu-id="8ba98-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8ba98-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ba98-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8ba98-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ba98-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba98-122">CommonParameters</span></span>
<span data-ttu-id="8ba98-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba98-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba98-124">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ba98-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba98-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ba98-125">INPUTS</span></span>

### <span data-ttu-id="8ba98-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8ba98-126">System.String</span></span>

## <span data-ttu-id="8ba98-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ba98-127">OUTPUTS</span></span>

### <span data-ttu-id="8ba98-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8ba98-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="8ba98-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ba98-129">NOTES</span></span>

## <span data-ttu-id="8ba98-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ba98-130">RELATED LINKS</span></span>

[<span data-ttu-id="8ba98-131">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8ba98-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="8ba98-132">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8ba98-132">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)


