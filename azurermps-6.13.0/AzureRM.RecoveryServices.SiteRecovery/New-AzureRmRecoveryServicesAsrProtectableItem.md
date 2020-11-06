---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: c5d86909bffa7c38d66c31b56b34a66251b21d65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572663"
---
# <span data-ttu-id="0a84b-101">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0a84b-101">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="0a84b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a84b-102">SYNOPSIS</span></span>
<span data-ttu-id="0a84b-103">Lägga till (upptäcka) en fysisk server i listan över skydd bara objekt.</span><span class="sxs-lookup"><span data-stu-id="0a84b-103">Add(Discover) a physical server to the list of protectable items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a84b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a84b-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 -FriendlyName <String> -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a84b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a84b-105">DESCRIPTION</span></span>
<span data-ttu-id="0a84b-106">**New-AzureRmRecoveryServicesAsrProtectableItem** lägger till ett nytt skydd bara objekt i listan över identifierade skydds bara objekt i en skydds behållare i en ASR-Fabric (gäller endast för VMware Fabric-typen).</span><span class="sxs-lookup"><span data-stu-id="0a84b-106">The **New-AzureRmRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="0a84b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a84b-107">EXAMPLES</span></span>

### <span data-ttu-id="0a84b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0a84b-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="0a84b-109">Lägga till eller upptäck nya Azure Recovery Service-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="0a84b-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="0a84b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a84b-110">PARAMETERS</span></span>

### <span data-ttu-id="0a84b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a84b-111">-DefaultProfile</span></span>
<span data-ttu-id="0a84b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a84b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a84b-113">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0a84b-113">-FriendlyName</span></span>
<span data-ttu-id="0a84b-114">Eget namn för objektet som skyddas.</span><span class="sxs-lookup"><span data-stu-id="0a84b-114">Friendly name for the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a84b-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="0a84b-115">-IPAddress</span></span>
<span data-ttu-id="0a84b-116">IP-adress för den skydd bara artikeln.</span><span class="sxs-lookup"><span data-stu-id="0a84b-116">IP address of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a84b-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="0a84b-117">-OSType</span></span>
<span data-ttu-id="0a84b-118">Operativ system typ (Windows/Linux) för objektet som skyddas.</span><span class="sxs-lookup"><span data-stu-id="0a84b-118">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a84b-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0a84b-119">-ProtectionContainer</span></span>
<span data-ttu-id="0a84b-120">Behållarobjekt för automatisk system återställning där det skydd bara objektet ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="0a84b-120">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a84b-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0a84b-121">-Confirm</span></span>
<span data-ttu-id="0a84b-122">Fråga efter bekräftelse innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0a84b-122">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a84b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a84b-123">-WhatIf</span></span>
<span data-ttu-id="0a84b-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0a84b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a84b-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0a84b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a84b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a84b-126">CommonParameters</span></span>
<span data-ttu-id="0a84b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a84b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a84b-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a84b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a84b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a84b-129">INPUTS</span></span>

### <span data-ttu-id="0a84b-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0a84b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="0a84b-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a84b-131">OUTPUTS</span></span>

### <span data-ttu-id="0a84b-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0a84b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0a84b-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a84b-133">NOTES</span></span>

## <span data-ttu-id="0a84b-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a84b-134">RELATED LINKS</span></span>
