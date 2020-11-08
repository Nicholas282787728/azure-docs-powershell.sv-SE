---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1B1C1459-A602-423D-8CAA-B4901CFC2C82
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f684908e8119da007f8b1f844ebbac40713d51
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099709"
---
# <span data-ttu-id="3f49b-101">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3f49b-101">Remove-AzureDns</span></span>

## <span data-ttu-id="3f49b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f49b-102">SYNOPSIS</span></span>
<span data-ttu-id="3f49b-103">Tar bort en DNS-server från en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="3f49b-103">Removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="3f49b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f49b-104">SYNTAX</span></span>

```
Remove-AzureDns [-Name] <String> [-ServiceName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3f49b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f49b-105">DESCRIPTION</span></span>
<span data-ttu-id="3f49b-106">Cmdleten **Remove-AzureDns** tar bort en DNS-server från en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="3f49b-106">The **Remove-AzureDns** cmdlet removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="3f49b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f49b-107">EXAMPLES</span></span>

### <span data-ttu-id="3f49b-108">Exempel 1: ta bort en DNS-server från en tjänst</span><span class="sxs-lookup"><span data-stu-id="3f49b-108">Example 1: Remove a DNS server from a service</span></span>
```
PS C:\> Remove-AzureDns -ServiceName "ContosoService" -Name "Dns07"
```

<span data-ttu-id="3f49b-109">Det här kommandot tar bort DNS-servern som heter Dns07 från ContosoService.</span><span class="sxs-lookup"><span data-stu-id="3f49b-109">This command removes the DNS server named Dns07 from ContosoService.</span></span>

## <span data-ttu-id="3f49b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f49b-110">PARAMETERS</span></span>

### <span data-ttu-id="3f49b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3f49b-111">-Force</span></span>
<span data-ttu-id="3f49b-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3f49b-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f49b-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3f49b-113">-InformationAction</span></span>
<span data-ttu-id="3f49b-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="3f49b-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3f49b-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3f49b-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f49b-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="3f49b-116">Continue</span></span>
- <span data-ttu-id="3f49b-117">Över</span><span class="sxs-lookup"><span data-stu-id="3f49b-117">Ignore</span></span>
- <span data-ttu-id="3f49b-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="3f49b-118">Inquire</span></span>
- <span data-ttu-id="3f49b-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3f49b-119">SilentlyContinue</span></span>
- <span data-ttu-id="3f49b-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="3f49b-120">Stop</span></span>
- <span data-ttu-id="3f49b-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="3f49b-121">Suspend</span></span>

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

### <span data-ttu-id="3f49b-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3f49b-122">-InformationVariable</span></span>
<span data-ttu-id="3f49b-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="3f49b-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3f49b-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f49b-124">-Name</span></span>
<span data-ttu-id="3f49b-125">Anger namnet på den DNS-server som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="3f49b-125">Specifies the name of the DNS server that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3f49b-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="3f49b-126">-Profile</span></span>
<span data-ttu-id="3f49b-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3f49b-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f49b-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3f49b-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f49b-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3f49b-129">-ServiceName</span></span>
<span data-ttu-id="3f49b-130">Anger namnet på den tjänst som denna cmdlet tar bort en DNS-server från.</span><span class="sxs-lookup"><span data-stu-id="3f49b-130">Specifies the name of the service from which this cmdlet removes a DNS server.</span></span>

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

### <span data-ttu-id="3f49b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f49b-131">CommonParameters</span></span>
<span data-ttu-id="3f49b-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f49b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f49b-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f49b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f49b-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f49b-134">INPUTS</span></span>

## <span data-ttu-id="3f49b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f49b-135">OUTPUTS</span></span>

### <span data-ttu-id="3f49b-136">Microsoft. WindowsAzure. commands. Utilitiess. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="3f49b-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="3f49b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f49b-137">NOTES</span></span>

## <span data-ttu-id="3f49b-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f49b-138">RELATED LINKS</span></span>

[<span data-ttu-id="3f49b-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3f49b-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="3f49b-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3f49b-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="3f49b-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3f49b-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="3f49b-142">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="3f49b-142">Set-AzureDns</span></span>](./Set-AzureDns.md)


