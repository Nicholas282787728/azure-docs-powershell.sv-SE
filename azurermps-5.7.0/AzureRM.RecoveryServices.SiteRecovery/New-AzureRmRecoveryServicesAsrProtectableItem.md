---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 8973c3606c7c29c254650b3412275c1dfd7bf761
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583084"
---
# <span data-ttu-id="62e02-101">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="62e02-101">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="62e02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62e02-102">SYNOPSIS</span></span>
<span data-ttu-id="62e02-103">Lägga till (upptäcka) en fysisk server i listan över skydd bara objekt.</span><span class="sxs-lookup"><span data-stu-id="62e02-103">Add(Discover) a physical server to the list of protectable items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62e02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62e02-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 -FriendlyName <String> -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62e02-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62e02-105">DESCRIPTION</span></span>
<span data-ttu-id="62e02-106">**New-AzureRmRecoveryServicesAsrProtectableItem** lägger till ett nytt skydd bara objekt i listan över identifierade skydds bara objekt i en skydds behållare i en ASR-Fabric (gäller endast för VMware Fabric-typen).</span><span class="sxs-lookup"><span data-stu-id="62e02-106">The **New-AzureRmRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="62e02-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62e02-107">EXAMPLES</span></span>

### <span data-ttu-id="62e02-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="62e02-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectableItem ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="62e02-109">Lägga till eller upptäck nya Azure Recovery Service-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="62e02-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="62e02-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62e02-110">PARAMETERS</span></span>

### <span data-ttu-id="62e02-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62e02-111">-Confirm</span></span>
<span data-ttu-id="62e02-112">Fråga efter bekräftelse innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62e02-112">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e02-113">-DefaultProfile</span></span>
<span data-ttu-id="62e02-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62e02-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62e02-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="62e02-115">-FriendlyName</span></span>
<span data-ttu-id="62e02-116">Eget namn för objektet som skyddas.</span><span class="sxs-lookup"><span data-stu-id="62e02-116">Friendly name for the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e02-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="62e02-117">-IPAddress</span></span>
<span data-ttu-id="62e02-118">IP-adress för den skydd bara artikeln.</span><span class="sxs-lookup"><span data-stu-id="62e02-118">IP address of the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e02-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="62e02-119">-OSType</span></span>
<span data-ttu-id="62e02-120">Operativ system typ (Windows/Linux) för objektet som skyddas.</span><span class="sxs-lookup"><span data-stu-id="62e02-120">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e02-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="62e02-121">-ProtectionContainer</span></span>
<span data-ttu-id="62e02-122">Behållarobjekt för automatisk system återställning där det skydd bara objektet ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="62e02-122">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62e02-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e02-123">-WhatIf</span></span>
<span data-ttu-id="62e02-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62e02-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62e02-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62e02-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62e02-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e02-126">CommonParameters</span></span>
<span data-ttu-id="62e02-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62e02-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e02-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62e02-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e02-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62e02-129">INPUTS</span></span>

### <span data-ttu-id="62e02-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="62e02-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="62e02-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62e02-131">OUTPUTS</span></span>

### <span data-ttu-id="62e02-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="62e02-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="62e02-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62e02-133">NOTES</span></span>

## <span data-ttu-id="62e02-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62e02-134">RELATED LINKS</span></span>
