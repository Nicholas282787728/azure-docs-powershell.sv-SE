---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099154"
---
# <span data-ttu-id="59bca-101">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="59bca-101">New-AzureDns</span></span>

## <span data-ttu-id="59bca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59bca-102">SYNOPSIS</span></span>
<span data-ttu-id="59bca-103">Skapar ett objekt för Azure DNS Settings.</span><span class="sxs-lookup"><span data-stu-id="59bca-103">Creates an Azure DNS settings object.</span></span>

## <span data-ttu-id="59bca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59bca-104">SYNTAX</span></span>

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="59bca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59bca-105">DESCRIPTION</span></span>
<span data-ttu-id="59bca-106">Cmdleten **New-AzureDns** skapar ett Azure DNS Settings-objekt.</span><span class="sxs-lookup"><span data-stu-id="59bca-106">The **New-AzureDns** cmdlet creates an Azure DNS settings object.</span></span>
<span data-ttu-id="59bca-107">Du kan använda ett DNS-Setting-objekt när du skapar en virtuell dator med cmdleten **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="59bca-107">You can use a DNS settings object when you create a virtual machine by using the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="59bca-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59bca-108">EXAMPLES</span></span>

### <span data-ttu-id="59bca-109">Exempel 1: skapa ett objekt med DNS-inställningar</span><span class="sxs-lookup"><span data-stu-id="59bca-109">Example 1: Create a DNS settings object</span></span>
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

<span data-ttu-id="59bca-110">Det här kommandot skapar ett objekt för Azure DNS Settings.</span><span class="sxs-lookup"><span data-stu-id="59bca-110">This command creates an Azure DNS settings object.</span></span>
<span data-ttu-id="59bca-111">DNS-servern har den angivna adressen och det egna namnet Dns01.</span><span class="sxs-lookup"><span data-stu-id="59bca-111">The DNS server has the specified address and the friendly name Dns01.</span></span>
<span data-ttu-id="59bca-112">Kommandot lagrar objektet i $Dns variabel för användning av **New-AzureVM-** cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59bca-112">The command stores the object in the $Dns variable for use by the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="59bca-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59bca-113">PARAMETERS</span></span>

### <span data-ttu-id="59bca-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="59bca-114">-InformationAction</span></span>
<span data-ttu-id="59bca-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="59bca-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="59bca-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="59bca-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59bca-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="59bca-117">Continue</span></span>
- <span data-ttu-id="59bca-118">Över</span><span class="sxs-lookup"><span data-stu-id="59bca-118">Ignore</span></span>
- <span data-ttu-id="59bca-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="59bca-119">Inquire</span></span>
- <span data-ttu-id="59bca-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="59bca-120">SilentlyContinue</span></span>
- <span data-ttu-id="59bca-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="59bca-121">Stop</span></span>
- <span data-ttu-id="59bca-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="59bca-122">Suspend</span></span>

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

### <span data-ttu-id="59bca-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="59bca-123">-InformationVariable</span></span>
<span data-ttu-id="59bca-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="59bca-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="59bca-125">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="59bca-125">-IPAddress</span></span>
<span data-ttu-id="59bca-126">Anger DNS-serverns IP-adress.</span><span class="sxs-lookup"><span data-stu-id="59bca-126">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="59bca-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="59bca-127">-Name</span></span>
<span data-ttu-id="59bca-128">Anger ett eget namn för DNS-servern.</span><span class="sxs-lookup"><span data-stu-id="59bca-128">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="59bca-129">Det här namnet är inte nödvändigt vis ett fullständigt domän namn.</span><span class="sxs-lookup"><span data-stu-id="59bca-129">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="59bca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bca-130">CommonParameters</span></span>
<span data-ttu-id="59bca-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59bca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bca-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59bca-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bca-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59bca-133">INPUTS</span></span>

## <span data-ttu-id="59bca-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59bca-134">OUTPUTS</span></span>

## <span data-ttu-id="59bca-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59bca-135">NOTES</span></span>

## <span data-ttu-id="59bca-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59bca-136">RELATED LINKS</span></span>

[<span data-ttu-id="59bca-137">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="59bca-137">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="59bca-138">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="59bca-138">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="59bca-139">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="59bca-139">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="59bca-140">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="59bca-140">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="59bca-141">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="59bca-141">Set-AzureDns</span></span>](./Set-AzureDns.md)


