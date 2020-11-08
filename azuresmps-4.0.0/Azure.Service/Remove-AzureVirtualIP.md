---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B107D789-8F66-4D7D-B126-08ACB0364826
online version: ''
schema: 2.0.0
ms.openlocfilehash: e59df078539e9ea94073defd4c8ea13a69cc2e5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093213"
---
# <span data-ttu-id="56266-101">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="56266-101">Remove-AzureVirtualIP</span></span>

## <span data-ttu-id="56266-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56266-102">SYNOPSIS</span></span>
<span data-ttu-id="56266-103">Tar bort en virtuell IP-adress från din moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="56266-103">Deletes a virtual IP address from your Cloud Service.</span></span>

## <span data-ttu-id="56266-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56266-104">SYNTAX</span></span>

```
Remove-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="56266-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56266-105">DESCRIPTION</span></span>
<span data-ttu-id="56266-106">Cmdleten **Remove-AzureVirtualIP** tar bort en virtuell IP (VIP) från en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="56266-106">The **Remove-AzureVirtualIP** cmdlet deletes a virtual IP (VIP) from an Azure service.</span></span>
<span data-ttu-id="56266-107">Åtgärden fungerar bara om det inte finns några kopplade slut punkter för den virtuella IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="56266-107">The operation succeeds only if the virtual IP has no endpoints associated with it.</span></span>

## <span data-ttu-id="56266-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56266-108">EXAMPLES</span></span>

### <span data-ttu-id="56266-109">Exempel 1: ta bort en virtuell IP-adress från en tjänst</span><span class="sxs-lookup"><span data-stu-id="56266-109">Example 1: Remove a virtual IP address from a service</span></span>
```
PS C:\> Remove-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
```

<span data-ttu-id="56266-110">Det här kommandot tar bort en virtuell IP-adress från en tjänst.</span><span class="sxs-lookup"><span data-stu-id="56266-110">This command removes a virtual IP address from a service.</span></span>

## <span data-ttu-id="56266-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56266-111">PARAMETERS</span></span>

### <span data-ttu-id="56266-112">-Force</span><span class="sxs-lookup"><span data-stu-id="56266-112">-Force</span></span>
<span data-ttu-id="56266-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="56266-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56266-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="56266-114">-InformationAction</span></span>
<span data-ttu-id="56266-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="56266-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="56266-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="56266-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56266-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="56266-117">Continue</span></span>
- <span data-ttu-id="56266-118">Över</span><span class="sxs-lookup"><span data-stu-id="56266-118">Ignore</span></span>
- <span data-ttu-id="56266-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="56266-119">Inquire</span></span>
- <span data-ttu-id="56266-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="56266-120">SilentlyContinue</span></span>
- <span data-ttu-id="56266-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="56266-121">Stop</span></span>
- <span data-ttu-id="56266-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="56266-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56266-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="56266-123">-InformationVariable</span></span>
<span data-ttu-id="56266-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="56266-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56266-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="56266-125">-Profile</span></span>
<span data-ttu-id="56266-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="56266-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56266-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="56266-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56266-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="56266-128">-ServiceName</span></span>
<span data-ttu-id="56266-129">Anger namnet på den tjänst som du vill ta bort en virtuell IP-adress från.</span><span class="sxs-lookup"><span data-stu-id="56266-129">Specifies the name of the service from which to remove a virtual IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56266-130">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="56266-130">-VirtualIPName</span></span>
<span data-ttu-id="56266-131">Anger namnet på den virtuella IP-adressen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="56266-131">Specifies the name of the virtual IP address to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56266-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56266-132">CommonParameters</span></span>
<span data-ttu-id="56266-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56266-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56266-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56266-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56266-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56266-135">INPUTS</span></span>

## <span data-ttu-id="56266-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56266-136">OUTPUTS</span></span>

### <span data-ttu-id="56266-137">Microsoft. WindowsAzure. commands. Utilitiess. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="56266-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="56266-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56266-138">NOTES</span></span>

## <span data-ttu-id="56266-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56266-139">RELATED LINKS</span></span>

[<span data-ttu-id="56266-140">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="56266-140">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)


