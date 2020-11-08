---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BC16303-CCB4-40D8-ABCB-59CF0D85ED63
online version: ''
schema: 2.0.0
ms.openlocfilehash: f24f5d8f7f72c59847cfa5dde51a1937bc304735
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099299"
---
# <span data-ttu-id="35e5c-101">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="35e5c-101">Set-AzureDns</span></span>

## <span data-ttu-id="35e5c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="35e5c-103">Ändrar IP-adressen för en DNS-server.</span><span class="sxs-lookup"><span data-stu-id="35e5c-103">Modifies the IP address of a DNS server.</span></span>

## <span data-ttu-id="35e5c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35e5c-104">SYNTAX</span></span>

```
Set-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="35e5c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35e5c-105">DESCRIPTION</span></span>
<span data-ttu-id="35e5c-106">Cmdleten **set-AzureDns** ändrar IP-adressen för en DNS-server för en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="35e5c-106">The **Set-AzureDns** cmdlet modifies the IP address of a DNS server for an Azure service.</span></span>

## <span data-ttu-id="35e5c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35e5c-107">EXAMPLES</span></span>

### <span data-ttu-id="35e5c-108">Exempel 1: ändra IP-adressen för en DNS-Server</span><span class="sxs-lookup"><span data-stu-id="35e5c-108">Example 1: Modify the IP address of a DNS server</span></span>
```
PS C:\> Set-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.5 -Name "Dns07"
```

<span data-ttu-id="35e5c-109">Det här kommandot ändrar IP-adressen för DNS-servern med namnet Dns07 för tjänsten som heter ContosoService.</span><span class="sxs-lookup"><span data-stu-id="35e5c-109">This command modifies the IP address of the DNS server named Dns07 for the service named ContosoService.</span></span>

## <span data-ttu-id="35e5c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35e5c-110">PARAMETERS</span></span>

### <span data-ttu-id="35e5c-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="35e5c-111">-InformationAction</span></span>
<span data-ttu-id="35e5c-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="35e5c-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="35e5c-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="35e5c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35e5c-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="35e5c-114">Continue</span></span>
- <span data-ttu-id="35e5c-115">Över</span><span class="sxs-lookup"><span data-stu-id="35e5c-115">Ignore</span></span>
- <span data-ttu-id="35e5c-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="35e5c-116">Inquire</span></span>
- <span data-ttu-id="35e5c-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="35e5c-117">SilentlyContinue</span></span>
- <span data-ttu-id="35e5c-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="35e5c-118">Stop</span></span>
- <span data-ttu-id="35e5c-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="35e5c-119">Suspend</span></span>

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

### <span data-ttu-id="35e5c-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="35e5c-120">-InformationVariable</span></span>
<span data-ttu-id="35e5c-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="35e5c-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="35e5c-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="35e5c-122">-IPAddress</span></span>
<span data-ttu-id="35e5c-123">Anger den nya IP-adressen för DNS-servern.</span><span class="sxs-lookup"><span data-stu-id="35e5c-123">Specifies the new IP address of the DNS server.</span></span>

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

### <span data-ttu-id="35e5c-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="35e5c-124">-Name</span></span>
<span data-ttu-id="35e5c-125">Anger namnet på den DNS-server som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="35e5c-125">Specifies the name of the DNS server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35e5c-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="35e5c-126">-Profile</span></span>
<span data-ttu-id="35e5c-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="35e5c-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="35e5c-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="35e5c-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="35e5c-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="35e5c-129">-ServiceName</span></span>
<span data-ttu-id="35e5c-130">Anger namnet på den tjänst där denna cmdlet ändrar DNS-serverns adress.</span><span class="sxs-lookup"><span data-stu-id="35e5c-130">Specifies the name of the service for which this cmdlet modifies the address of the DNS server.</span></span>

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

### <span data-ttu-id="35e5c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e5c-131">CommonParameters</span></span>
<span data-ttu-id="35e5c-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35e5c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e5c-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35e5c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e5c-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35e5c-134">INPUTS</span></span>

## <span data-ttu-id="35e5c-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35e5c-135">OUTPUTS</span></span>

### <span data-ttu-id="35e5c-136">Microsoft. WindowsAzure. commands. Utilitiess. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="35e5c-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="35e5c-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35e5c-137">NOTES</span></span>

## <span data-ttu-id="35e5c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35e5c-138">RELATED LINKS</span></span>

[<span data-ttu-id="35e5c-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="35e5c-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="35e5c-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="35e5c-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="35e5c-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="35e5c-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="35e5c-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="35e5c-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)


