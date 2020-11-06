---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 298443c4b962a2be6c5cf3849657d0fe8bbaf978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574192"
---
# <span data-ttu-id="12931-101">Update-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="12931-101">Update-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="12931-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12931-102">SYNOPSIS</span></span>
<span data-ttu-id="12931-103">Uppdatera identifierings information för en registrerad vCenter.</span><span class="sxs-lookup"><span data-stu-id="12931-103">Update discovery details for a registered vCenter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12931-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12931-104">SYNTAX</span></span>

### <span data-ttu-id="12931-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="12931-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12931-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="12931-106">ByResourceId</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12931-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12931-107">DESCRIPTION</span></span>
<span data-ttu-id="12931-108">Cmdleten **Update-AzureRmRecoveryServicesAsrvCenter** uppdaterar identifierings information för en registrerad vCenter.</span><span class="sxs-lookup"><span data-stu-id="12931-108">The **Update-AzureRmRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="12931-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12931-109">EXAMPLES</span></span>

### <span data-ttu-id="12931-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="12931-110">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="12931-111">Uppdatera identifierings information för en registrerad vCenter.</span><span class="sxs-lookup"><span data-stu-id="12931-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="12931-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12931-112">PARAMETERS</span></span>

### <span data-ttu-id="12931-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="12931-113">-Account</span></span>
<span data-ttu-id="12931-114">konto för inloggnings uppgifter för vCenter.</span><span class="sxs-lookup"><span data-stu-id="12931-114">vCenter login credentials account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12931-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12931-115">-Confirm</span></span>
<span data-ttu-id="12931-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12931-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12931-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12931-117">-DefaultProfile</span></span>
<span data-ttu-id="12931-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12931-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12931-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12931-119">-InputObject</span></span>
<span data-ttu-id="12931-120">VCenter-serverobjektet för att uppdatera identifierings information för.</span><span class="sxs-lookup"><span data-stu-id="12931-120">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12931-121">-Port</span><span class="sxs-lookup"><span data-stu-id="12931-121">-Port</span></span>
<span data-ttu-id="12931-122">TCP-porten på vCenter-servern som ska användas för identifiering.</span><span class="sxs-lookup"><span data-stu-id="12931-122">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12931-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12931-123">-ResourceId</span></span>
<span data-ttu-id="12931-124">Anger resourceId för vCenter.</span><span class="sxs-lookup"><span data-stu-id="12931-124">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12931-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12931-125">-WhatIf</span></span>
<span data-ttu-id="12931-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12931-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12931-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12931-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12931-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12931-128">CommonParameters</span></span>
<span data-ttu-id="12931-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12931-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12931-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12931-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12931-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12931-131">INPUTS</span></span>

### <span data-ttu-id="12931-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="12931-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="12931-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12931-133">OUTPUTS</span></span>

### <span data-ttu-id="12931-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 0.1.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="12931-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="12931-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12931-135">NOTES</span></span>

## <span data-ttu-id="12931-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12931-136">RELATED LINKS</span></span>
