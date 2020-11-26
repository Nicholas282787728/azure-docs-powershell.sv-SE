---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271230"
---
# <span data-ttu-id="7493c-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="7493c-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="7493c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7493c-102">SYNOPSIS</span></span>
<span data-ttu-id="7493c-103">Uppdaterar inställning för automatisk etablering</span><span class="sxs-lookup"><span data-stu-id="7493c-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="7493c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7493c-104">SYNTAX</span></span>

### <span data-ttu-id="7493c-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="7493c-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7493c-106">ID</span><span class="sxs-lookup"><span data-stu-id="7493c-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7493c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7493c-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7493c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7493c-108">DESCRIPTION</span></span>
<span data-ttu-id="7493c-109">Aktiverar eller inaktiverar automatisk konfigurations inställningar för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="7493c-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="7493c-110">Med inställningarna för automatisk etablering kan du bestämma om du vill att Azure Security Center automatiskt ska tillhandahålla en säkerhets agent som installeras på din dator.</span><span class="sxs-lookup"><span data-stu-id="7493c-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="7493c-111">Säkerhets agenten övervakar din virtuella dator för att skapa säkerhets varningar och övervaka den virtuella datorns säkerhetskompatibilitet.</span><span class="sxs-lookup"><span data-stu-id="7493c-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="7493c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7493c-112">EXAMPLES</span></span>

### <span data-ttu-id="7493c-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7493c-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="7493c-114">Aktiverar automatisk etablerings inställning för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="7493c-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="7493c-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7493c-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="7493c-116">Inaktiverar automatisk konfigurations inställning för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="7493c-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="7493c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7493c-117">PARAMETERS</span></span>

### <span data-ttu-id="7493c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7493c-118">-DefaultProfile</span></span>
<span data-ttu-id="7493c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7493c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7493c-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="7493c-120">-EnableAutoProvision</span></span>
<span data-ttu-id="7493c-121">Automatisk etablering.</span><span class="sxs-lookup"><span data-stu-id="7493c-121">Automatic Provisioning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7493c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7493c-122">-InputObject</span></span>
<span data-ttu-id="7493c-123">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="7493c-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7493c-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="7493c-124">-Name</span></span>
<span data-ttu-id="7493c-125">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="7493c-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7493c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7493c-126">-ResourceId</span></span>
<span data-ttu-id="7493c-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7493c-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7493c-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7493c-128">-Confirm</span></span>
<span data-ttu-id="7493c-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7493c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7493c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7493c-130">-WhatIf</span></span>
<span data-ttu-id="7493c-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7493c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7493c-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7493c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7493c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7493c-133">CommonParameters</span></span>
<span data-ttu-id="7493c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7493c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7493c-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7493c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7493c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7493c-136">INPUTS</span></span>

### <span data-ttu-id="7493c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7493c-137">System.String</span></span>

### <span data-ttu-id="7493c-138">Microsoft. Azure. commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="7493c-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="7493c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7493c-139">OUTPUTS</span></span>

### <span data-ttu-id="7493c-140">Microsoft. Azure. commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="7493c-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="7493c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7493c-141">NOTES</span></span>

## <span data-ttu-id="7493c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7493c-142">RELATED LINKS</span></span>