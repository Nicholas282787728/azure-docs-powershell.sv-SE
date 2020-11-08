---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 184FB33A-C866-4AF0-BA31-8ADCFC6EE8E2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ce5d8511383ad93e288b97381416d7864c3f80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093372"
---
# <span data-ttu-id="c5049-101">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="c5049-101">Get-AzureDns</span></span>

## <span data-ttu-id="c5049-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5049-102">SYNOPSIS</span></span>
<span data-ttu-id="c5049-103">Hämtar DNS-inställningarna för en Azure-distribution.</span><span class="sxs-lookup"><span data-stu-id="c5049-103">Gets the DNS settings for an Azure deployment.</span></span>

## <span data-ttu-id="c5049-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5049-104">SYNTAX</span></span>

```
Get-AzureDns [-DnsSettings <DnsSettings>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c5049-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5049-105">DESCRIPTION</span></span>
<span data-ttu-id="c5049-106">Cmdleten **Get-AzureDns** hämtar DNS-inställningarna för en Azure-distribution.</span><span class="sxs-lookup"><span data-stu-id="c5049-106">The **Get-AzureDns** cmdlet gets the DNS settings for an Azure deployment.</span></span>
<span data-ttu-id="c5049-107">Cmdleten returnerar DNS-serverns eget namn och IP-adress i ett DNS Settings-objekt.</span><span class="sxs-lookup"><span data-stu-id="c5049-107">The cmdlet returns the friendly name and IP address of the DNS server in a DNS settings object.</span></span>

## <span data-ttu-id="c5049-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5049-108">EXAMPLES</span></span>

### <span data-ttu-id="c5049-109">Exempel 1: Hämta DNS-inställningar</span><span class="sxs-lookup"><span data-stu-id="c5049-109">Example 1: Get DNS settings</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Production" | Get-AzureDNS
```

<span data-ttu-id="c5049-110">Det här kommandot använder cmdleten **Get-AzureDeployment** för att få produktions distributionen av tjänsten som heter ContosoService.</span><span class="sxs-lookup"><span data-stu-id="c5049-110">This command uses the **Get-AzureDeployment** cmdlet to get the production deployment of the service named ContosoService.</span></span>
<span data-ttu-id="c5049-111">Kommandot skickar detta objekt till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="c5049-111">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c5049-112">Den aktuella cmdleten får DNS-inställningarna.</span><span class="sxs-lookup"><span data-stu-id="c5049-112">The current cmdlet gets the DNS settings.</span></span>

## <span data-ttu-id="c5049-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5049-113">PARAMETERS</span></span>

### <span data-ttu-id="c5049-114">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="c5049-114">-DnsSettings</span></span>
<span data-ttu-id="c5049-115">Anger ett **DnsSettings** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c5049-115">Specifies a **DnsSettings** object.</span></span>

```yaml
Type: DnsSettings
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5049-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c5049-116">-InformationAction</span></span>
<span data-ttu-id="c5049-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c5049-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c5049-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c5049-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c5049-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="c5049-119">Continue</span></span>
- <span data-ttu-id="c5049-120">Över</span><span class="sxs-lookup"><span data-stu-id="c5049-120">Ignore</span></span>
- <span data-ttu-id="c5049-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="c5049-121">Inquire</span></span>
- <span data-ttu-id="c5049-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c5049-122">SilentlyContinue</span></span>
- <span data-ttu-id="c5049-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="c5049-123">Stop</span></span>
- <span data-ttu-id="c5049-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c5049-124">Suspend</span></span>

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

### <span data-ttu-id="c5049-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c5049-125">-InformationVariable</span></span>
<span data-ttu-id="c5049-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c5049-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c5049-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5049-127">CommonParameters</span></span>
<span data-ttu-id="c5049-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5049-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5049-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5049-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5049-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5049-130">INPUTS</span></span>

## <span data-ttu-id="c5049-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5049-131">OUTPUTS</span></span>

## <span data-ttu-id="c5049-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5049-132">NOTES</span></span>

## <span data-ttu-id="c5049-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5049-133">RELATED LINKS</span></span>

[<span data-ttu-id="c5049-134">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="c5049-134">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="c5049-135">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c5049-135">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="c5049-136">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="c5049-136">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="c5049-137">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="c5049-137">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="c5049-138">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="c5049-138">Set-AzureDns</span></span>](./Set-AzureDns.md)


