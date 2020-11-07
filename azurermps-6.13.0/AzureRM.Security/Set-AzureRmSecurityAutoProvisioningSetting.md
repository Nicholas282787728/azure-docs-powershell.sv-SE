---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: e99ead17cad0a3c6c440967ec1b1852bb5568a26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755810"
---
# <span data-ttu-id="43cdc-101">Set-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="43cdc-101">Set-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="43cdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="43cdc-103">Uppdaterar inställning för automatisk etablering</span><span class="sxs-lookup"><span data-stu-id="43cdc-103">Updates automatic provisioning setting</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43cdc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43cdc-104">SYNTAX</span></span>

### <span data-ttu-id="43cdc-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="43cdc-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43cdc-106">ID</span><span class="sxs-lookup"><span data-stu-id="43cdc-106">ResourceId</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43cdc-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="43cdc-107">InputObject</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43cdc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43cdc-108">DESCRIPTION</span></span>
<span data-ttu-id="43cdc-109">Aktiverar eller inaktiverar automatisk konfigurations inställningar för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="43cdc-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="43cdc-110">Med inställningarna för automatisk etablering kan du bestämma om du vill att Azure Security Center automatiskt ska tillhandahålla en säkerhets agent som installeras på din dator.</span><span class="sxs-lookup"><span data-stu-id="43cdc-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="43cdc-111">Säkerhets agenten övervakar din virtuella dator för att skapa säkerhets varningar och övervaka den virtuella datorns säkerhetskompatibilitet.</span><span class="sxs-lookup"><span data-stu-id="43cdc-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="43cdc-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43cdc-112">EXAMPLES</span></span>

### <span data-ttu-id="43cdc-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="43cdc-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="43cdc-114">Aktiverar automatisk etablerings inställning för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="43cdc-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="43cdc-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="43cdc-115">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="43cdc-116">Inaktiverar automatisk konfigurations inställning för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="43cdc-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="43cdc-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43cdc-117">PARAMETERS</span></span>

### <span data-ttu-id="43cdc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43cdc-118">-DefaultProfile</span></span>
<span data-ttu-id="43cdc-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43cdc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43cdc-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="43cdc-120">-EnableAutoProvision</span></span>
<span data-ttu-id="43cdc-121">Automatisk etablering.</span><span class="sxs-lookup"><span data-stu-id="43cdc-121">Automatic Provisioning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43cdc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43cdc-122">-InputObject</span></span>
<span data-ttu-id="43cdc-123">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="43cdc-123">Input Object.</span></span>

```yaml
Type: PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43cdc-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="43cdc-124">-Name</span></span>
<span data-ttu-id="43cdc-125">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="43cdc-125">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43cdc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43cdc-126">-ResourceId</span></span>
<span data-ttu-id="43cdc-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="43cdc-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43cdc-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43cdc-128">-Confirm</span></span>
<span data-ttu-id="43cdc-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43cdc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43cdc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43cdc-130">-WhatIf</span></span>
<span data-ttu-id="43cdc-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43cdc-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43cdc-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43cdc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43cdc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43cdc-133">CommonParameters</span></span>
<span data-ttu-id="43cdc-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43cdc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43cdc-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43cdc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43cdc-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43cdc-136">INPUTS</span></span>

### <span data-ttu-id="43cdc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="43cdc-137">System.String</span></span>
<span data-ttu-id="43cdc-138">System. Management. Automation. SwitchParameter Microsoft. Azure. commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="43cdc-138">System.Management.Automation.SwitchParameter Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="43cdc-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43cdc-139">OUTPUTS</span></span>

### <span data-ttu-id="43cdc-140">Microsoft. Azure. commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="43cdc-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="43cdc-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43cdc-141">NOTES</span></span>

## <span data-ttu-id="43cdc-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43cdc-142">RELATED LINKS</span></span>
