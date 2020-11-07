---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 57f9009ead66eb87685aaf0142c6dbd8b125f307
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747387"
---
# <span data-ttu-id="e1d8d-101">New-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e1d8d-101">New-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="e1d8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d8d-103">Lägga till (upptäcka) en fysisk server i listan över skydd bara objekt.</span><span class="sxs-lookup"><span data-stu-id="e1d8d-103">Add(Discover) a physical server to the list of protectable items.</span></span>

## <span data-ttu-id="e1d8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1d8d-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer> -FriendlyName <String>
 -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1d8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1d8d-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d8d-106">**New-AzRecoveryServicesAsrProtectableItem** lägger till ett nytt skydd bara objekt i listan över identifierade skydds bara objekt i en skydds behållare i en ASR-Fabric (gäller endast för VMware Fabric-typen).</span><span class="sxs-lookup"><span data-stu-id="e1d8d-106">The **New-AzRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="e1d8d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1d8d-107">EXAMPLES</span></span>

### <span data-ttu-id="e1d8d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e1d8d-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="e1d8d-109">Lägga till eller upptäck nya Azure Recovery Service-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="e1d8d-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="e1d8d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1d8d-110">PARAMETERS</span></span>

### <span data-ttu-id="e1d8d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d8d-111">-DefaultProfile</span></span>
<span data-ttu-id="e1d8d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d8d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d8d-113">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e1d8d-113">-FriendlyName</span></span>
<span data-ttu-id="e1d8d-114">Eget namn för objektet som skyddas.</span><span class="sxs-lookup"><span data-stu-id="e1d8d-114">Friendly name for the protectable item.</span></span>

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

### <span data-ttu-id="e1d8d-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="e1d8d-115">-IPAddress</span></span>
<span data-ttu-id="e1d8d-116">IP-adress för den skydd bara artikeln.</span><span class="sxs-lookup"><span data-stu-id="e1d8d-116">IP address of the protectable item.</span></span>

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

### <span data-ttu-id="e1d8d-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="e1d8d-117">-OSType</span></span>
<span data-ttu-id="e1d8d-118">Operativ system typ (Windows/Linux) för objektet som skyddas.</span><span class="sxs-lookup"><span data-stu-id="e1d8d-118">Operating System type (Windows/Linux) of the protectable item.</span></span>

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

### <span data-ttu-id="e1d8d-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e1d8d-119">-ProtectionContainer</span></span>
<span data-ttu-id="e1d8d-120">Behållarobjekt för automatisk system återställning där det skydd bara objektet ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="e1d8d-120">ASR Protection container object to which the protectable item should be added.</span></span>

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

### <span data-ttu-id="e1d8d-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1d8d-121">-Confirm</span></span>
<span data-ttu-id="e1d8d-122">Fråga efter bekräftelse innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1d8d-122">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1d8d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1d8d-123">-WhatIf</span></span>
<span data-ttu-id="e1d8d-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1d8d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1d8d-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1d8d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1d8d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d8d-126">CommonParameters</span></span>
<span data-ttu-id="e1d8d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d8d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d8d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d8d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d8d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1d8d-129">INPUTS</span></span>

### <span data-ttu-id="e1d8d-130">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e1d8d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="e1d8d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1d8d-131">OUTPUTS</span></span>

### <span data-ttu-id="e1d8d-132">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e1d8d-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e1d8d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1d8d-133">NOTES</span></span>

## <span data-ttu-id="e1d8d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1d8d-134">RELATED LINKS</span></span>
