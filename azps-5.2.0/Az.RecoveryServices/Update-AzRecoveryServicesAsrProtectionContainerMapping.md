---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393075"
---
# <span data-ttu-id="bd933-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="bd933-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="bd933-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd933-102">SYNOPSIS</span></span>
<span data-ttu-id="bd933-103">Uppdatera behållaren för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="bd933-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="bd933-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd933-104">SYNTAX</span></span>

### <span data-ttu-id="bd933-105">AzureToAzureEnableAutoUpdate (standard)</span><span class="sxs-lookup"><span data-stu-id="bd933-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd933-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="bd933-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd933-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd933-107">DESCRIPTION</span></span>
<span data-ttu-id="bd933-108">Cmdleten **Update-AzRecoveryServicesAsrProtectionContainerMapping** uppdaterar den angivna mappningen för Azure Site Recovery-skydd.</span><span class="sxs-lookup"><span data-stu-id="bd933-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="bd933-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd933-109">EXAMPLES</span></span>

### <span data-ttu-id="bd933-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bd933-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="bd933-111">Starta åtgärden för att inaktivera automatisk uppdatering för behållaren.</span><span class="sxs-lookup"><span data-stu-id="bd933-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="bd933-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bd933-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="bd933-113">Starta operationen för att inaktivera aktivera automatisk uppdatering för behållaren.</span><span class="sxs-lookup"><span data-stu-id="bd933-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="bd933-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd933-114">PARAMETERS</span></span>

### <span data-ttu-id="bd933-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="bd933-115">-AutomationAccountId</span></span>
<span data-ttu-id="bd933-116">Anger den Automation accountId som används för automatiska UDPATE.</span><span class="sxs-lookup"><span data-stu-id="bd933-116">Specifies the automation accountId used for auto udpate.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd933-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="bd933-117">-AzureToAzure</span></span>
<span data-ttu-id="bd933-118">Anger Azure-till-Azure-skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="bd933-118">Specifies Azure to Azure protection container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd933-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd933-119">-DefaultProfile</span></span>
<span data-ttu-id="bd933-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd933-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd933-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="bd933-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="bd933-122">Växla parameter för att inaktivera automatisk uppdatering.</span><span class="sxs-lookup"><span data-stu-id="bd933-122">Switch parameter to disable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureDisableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd933-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="bd933-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="bd933-124">Växla parameter för att aktivera automatisk uppdatering.</span><span class="sxs-lookup"><span data-stu-id="bd933-124">Switch parameter to enable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd933-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd933-125">-InputObject</span></span>
<span data-ttu-id="bd933-126">Objekt för mappning av skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="bd933-126">Object for protection container mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd933-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd933-127">-Confirm</span></span>
<span data-ttu-id="bd933-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd933-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd933-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd933-129">-WhatIf</span></span>
<span data-ttu-id="bd933-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd933-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd933-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd933-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd933-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd933-132">CommonParameters</span></span>
<span data-ttu-id="bd933-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd933-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd933-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd933-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd933-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd933-135">INPUTS</span></span>

### <span data-ttu-id="bd933-136">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="bd933-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="bd933-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd933-137">OUTPUTS</span></span>

### <span data-ttu-id="bd933-138">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bd933-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bd933-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd933-139">NOTES</span></span>

## <span data-ttu-id="bd933-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd933-140">RELATED LINKS</span></span>
