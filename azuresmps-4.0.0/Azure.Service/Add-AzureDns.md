---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AF4DF7EC-95BA-44E2-AB9B-5C8FE45CCE4C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83c0858d813c157301098f680fa9d2a90ef6950a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093460"
---
# <span data-ttu-id="eb7aa-101">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="eb7aa-101">Add-AzureDns</span></span>

## <span data-ttu-id="eb7aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb7aa-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7aa-103">Lägger till en DNS-server till en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="eb7aa-103">Adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="eb7aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb7aa-104">SYNTAX</span></span>

```
Add-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eb7aa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb7aa-105">DESCRIPTION</span></span>
<span data-ttu-id="eb7aa-106">Cmdleten **Add-AzureDns** lägger till en DNS-server till en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="eb7aa-106">The **Add-AzureDns** cmdlet adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="eb7aa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb7aa-107">EXAMPLES</span></span>

### <span data-ttu-id="eb7aa-108">Exempel 1: lägga till en DNS-Server</span><span class="sxs-lookup"><span data-stu-id="eb7aa-108">Example 1: Add a DNS server</span></span>
```
PS C:\> Add-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.4 -Name "Dns07"
```

<span data-ttu-id="eb7aa-109">Det här kommandot lägger till DNS-servern som har adressen 10.1.2.4 till ContosoService.</span><span class="sxs-lookup"><span data-stu-id="eb7aa-109">This command adds the DNS server that has the address 10.1.2.4 to ContosoService.</span></span>

## <span data-ttu-id="eb7aa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb7aa-110">PARAMETERS</span></span>

### <span data-ttu-id="eb7aa-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="eb7aa-111">-InformationAction</span></span>
<span data-ttu-id="eb7aa-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="eb7aa-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eb7aa-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="eb7aa-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb7aa-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="eb7aa-114">Continue</span></span>
- <span data-ttu-id="eb7aa-115">Över</span><span class="sxs-lookup"><span data-stu-id="eb7aa-115">Ignore</span></span>
- <span data-ttu-id="eb7aa-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="eb7aa-116">Inquire</span></span>
- <span data-ttu-id="eb7aa-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eb7aa-117">SilentlyContinue</span></span>
- <span data-ttu-id="eb7aa-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="eb7aa-118">Stop</span></span>
- <span data-ttu-id="eb7aa-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="eb7aa-119">Suspend</span></span>

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

### <span data-ttu-id="eb7aa-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eb7aa-120">-InformationVariable</span></span>
<span data-ttu-id="eb7aa-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="eb7aa-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="eb7aa-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="eb7aa-122">-IPAddress</span></span>
<span data-ttu-id="eb7aa-123">Anger DNS-serverns IP-adress.</span><span class="sxs-lookup"><span data-stu-id="eb7aa-123">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="eb7aa-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb7aa-124">-Name</span></span>
<span data-ttu-id="eb7aa-125">Anger ett eget namn för DNS-servern.</span><span class="sxs-lookup"><span data-stu-id="eb7aa-125">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="eb7aa-126">Det här namnet är inte nödvändigt vis ett fullständigt domän namn.</span><span class="sxs-lookup"><span data-stu-id="eb7aa-126">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="eb7aa-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="eb7aa-127">-Profile</span></span>
<span data-ttu-id="eb7aa-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="eb7aa-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eb7aa-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="eb7aa-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eb7aa-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="eb7aa-130">-ServiceName</span></span>
<span data-ttu-id="eb7aa-131">Anger namnet på den tjänst där denna cmdlet lägger till DNS-servern.</span><span class="sxs-lookup"><span data-stu-id="eb7aa-131">Specifies the name of the service to which this cmdlet adds the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7aa-132">CommonParameters</span></span>
<span data-ttu-id="eb7aa-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb7aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7aa-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb7aa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7aa-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb7aa-135">INPUTS</span></span>

## <span data-ttu-id="eb7aa-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb7aa-136">OUTPUTS</span></span>

### <span data-ttu-id="eb7aa-137">Microsoft. WindowsAzure. commands. Utilitiess. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="eb7aa-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="eb7aa-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb7aa-138">NOTES</span></span>

## <span data-ttu-id="eb7aa-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb7aa-139">RELATED LINKS</span></span>

[<span data-ttu-id="eb7aa-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="eb7aa-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="eb7aa-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="eb7aa-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="eb7aa-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="eb7aa-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="eb7aa-143">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="eb7aa-143">Set-AzureDns</span></span>](./Set-AzureDns.md)


