---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 895F9A5F-D48F-403D-BD8F-72D72D420690
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97bb3e07f5c6df25e7c03c167cc4cb49c25f9414
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099017"
---
# <span data-ttu-id="31779-101">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="31779-101">Set-AzureVNetConfig</span></span>

## <span data-ttu-id="31779-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31779-102">SYNOPSIS</span></span>
<span data-ttu-id="31779-103">Uppdaterar inställningarna för det virtuella nätverket för en Azure Cloud-tjänst.</span><span class="sxs-lookup"><span data-stu-id="31779-103">Updates the virtual network settings for an Azure cloud service.</span></span>

## <span data-ttu-id="31779-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31779-104">SYNTAX</span></span>

```
Set-AzureVNetConfig [-ConfigurationPath] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="31779-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31779-105">DESCRIPTION</span></span>
<span data-ttu-id="31779-106">Cmdleten **set-AzureVNetConfig** uppdaterar nätverks konfigurationen för det aktuella Azure-abonnemanget genom att ange en sökväg till en nätverks konfigurations fil (. netcfg).</span><span class="sxs-lookup"><span data-stu-id="31779-106">The **Set-AzureVNetConfig** cmdlet updates the network configuration for the current Azure subscription by specifying a path to a network configuration file (.netcfg).</span></span>
<span data-ttu-id="31779-107">Nätverks konfigurations filen definierar DNS-servrar och undernät för moln tjänster inom ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="31779-107">The network configuration file defines DNS servers and subnets for cloud services within a subscription.</span></span>

## <span data-ttu-id="31779-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31779-108">EXAMPLES</span></span>

### <span data-ttu-id="31779-109">Exempel 1: uppdatera nätverks konfigurationen för Azure-prenumerationen till en lokal fil</span><span class="sxs-lookup"><span data-stu-id="31779-109">Example 1: Update the network configuration of the Azure subscription to a local file</span></span>
```
PS C:\> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="31779-110">Det här kommandot uppdaterar nätverks konfigurationen för den aktuella Microsoft Azure-prenumerationen till den lokala filen "c:\temp\MyAzNets.netcfg".</span><span class="sxs-lookup"><span data-stu-id="31779-110">This command updates the network configuration of the current Microsoft Azure subscription to that in the local file "c:\temp\MyAzNets.netcfg".</span></span>

### <span data-ttu-id="31779-111">Exempel 2: Ställ in Azure-abonnemanget och uppdatera nätverks konfigurationen</span><span class="sxs-lookup"><span data-stu-id="31779-111">Example 2: Set the Azure subscription and then update the network configuration</span></span>
```
PS C:\> $SubsId = "5bea2bc2-88a5-44b8-abe1-3e76733b6783"
C:\PS> $Cert = Get-Item cert:\LocalMachine\MY\82F105B2DA81149204A6257A9A91EC452B8C52C3
C:\PS> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="31779-112">I det här exemplet anges Microsoft Azure-prenumerationen och sedan uppdateras nätverks konfigurationen för abonnemanget med den konfiguration som definierats i den lokala filen "c:\temp\MyAzNets.netcfg".</span><span class="sxs-lookup"><span data-stu-id="31779-112">This example sets the Microsoft Azure subscription, and then updates the network configuration of that subscription using the configuration defined in the local file "c:\temp\MyAzNets.netcfg".</span></span>

## <span data-ttu-id="31779-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31779-113">PARAMETERS</span></span>

### <span data-ttu-id="31779-114">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="31779-114">-ConfigurationPath</span></span>
<span data-ttu-id="31779-115">Anger sökväg och fil namn för en nätverks konfigurations fil (. netcfg).</span><span class="sxs-lookup"><span data-stu-id="31779-115">Specifies the path and file name of a network configuration file (.netcfg).</span></span>

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

### <span data-ttu-id="31779-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="31779-116">-InformationAction</span></span>
<span data-ttu-id="31779-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="31779-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="31779-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="31779-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31779-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="31779-119">Continue</span></span>
- <span data-ttu-id="31779-120">Över</span><span class="sxs-lookup"><span data-stu-id="31779-120">Ignore</span></span>
- <span data-ttu-id="31779-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="31779-121">Inquire</span></span>
- <span data-ttu-id="31779-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="31779-122">SilentlyContinue</span></span>
- <span data-ttu-id="31779-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="31779-123">Stop</span></span>
- <span data-ttu-id="31779-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="31779-124">Suspend</span></span>

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

### <span data-ttu-id="31779-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="31779-125">-InformationVariable</span></span>
<span data-ttu-id="31779-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="31779-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="31779-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="31779-127">-Profile</span></span>
<span data-ttu-id="31779-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="31779-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="31779-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="31779-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="31779-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31779-130">CommonParameters</span></span>
<span data-ttu-id="31779-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31779-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31779-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31779-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31779-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31779-133">INPUTS</span></span>

## <span data-ttu-id="31779-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31779-134">OUTPUTS</span></span>

## <span data-ttu-id="31779-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31779-135">NOTES</span></span>

## <span data-ttu-id="31779-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31779-136">RELATED LINKS</span></span>

[<span data-ttu-id="31779-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="31779-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="31779-138">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="31779-138">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="31779-139">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="31779-139">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)


