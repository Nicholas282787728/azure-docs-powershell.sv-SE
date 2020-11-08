---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093351"
---
# <span data-ttu-id="b8beb-101">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="b8beb-101">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>

## <span data-ttu-id="b8beb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8beb-102">SYNOPSIS</span></span>
<span data-ttu-id="b8beb-103">Hämtar konfigurations skriptet för en Azure RemoteApp VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="b8beb-103">Retrieves the configuration script for an Azure RemoteApp VPN device.</span></span>

## <span data-ttu-id="b8beb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8beb-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b8beb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8beb-105">DESCRIPTION</span></span>
<span data-ttu-id="b8beb-106">Cmdleten **Get-AzureRemoteAppVpnDeviceConfigScript** hämtar konfigurations skriptet för en Azure RemoteApp-enhet med virtuellt privat nätverk (VPN).</span><span class="sxs-lookup"><span data-stu-id="b8beb-106">The **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet retrieves the configuration script for an Azure RemoteApp virtual private network (VPN) device.</span></span>

## <span data-ttu-id="b8beb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8beb-107">EXAMPLES</span></span>

### <span data-ttu-id="b8beb-108">Exempel 1: Hämta ett konfigurations skript för en VPN-enhet</span><span class="sxs-lookup"><span data-stu-id="b8beb-108">Example 1: Get a configuration script for a VPN device</span></span>
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

<span data-ttu-id="b8beb-109">Det här kommandot returnerar det skript eller den konfigurations fil som används för att konfigurera VPN-enheten för det virtuella nätverket med namnet ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="b8beb-109">This command returns the script or configuration file used to configure the VPN device for the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="b8beb-110">Det här manuset eller den här konfigurations filen bör köras eller laddas till VPN-enheten på vanligt sätt för den enheten.</span><span class="sxs-lookup"><span data-stu-id="b8beb-110">This script or configuration file should be run or loaded onto the VPN device in the typical manner for that device.</span></span>
<span data-ttu-id="b8beb-111">Kontakta VPN-enhetens tillverkare för att få unika krav för varje enhet.</span><span class="sxs-lookup"><span data-stu-id="b8beb-111">Consult the VPN device vendor for the unique requirements for each device.</span></span>

## <span data-ttu-id="b8beb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8beb-112">PARAMETERS</span></span>

### <span data-ttu-id="b8beb-113">-OSFamily</span><span class="sxs-lookup"><span data-stu-id="b8beb-113">-OSFamily</span></span>
<span data-ttu-id="b8beb-114">Anger operativ system familjen som körs på enhetens plattform.</span><span class="sxs-lookup"><span data-stu-id="b8beb-114">Specifies the operating system (OS) family that runs on the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8beb-115">-Platform</span><span class="sxs-lookup"><span data-stu-id="b8beb-115">-Platform</span></span>
<span data-ttu-id="b8beb-116">Anger enhetens plattform.</span><span class="sxs-lookup"><span data-stu-id="b8beb-116">Specifies the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8beb-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="b8beb-117">-Profile</span></span>
<span data-ttu-id="b8beb-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b8beb-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b8beb-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b8beb-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b8beb-120">-Vendor</span><span class="sxs-lookup"><span data-stu-id="b8beb-120">-Vendor</span></span>
<span data-ttu-id="b8beb-121">Anger leverantör för VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="b8beb-121">Specifies the vendor of the VPN device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8beb-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="b8beb-122">-VNetName</span></span>
<span data-ttu-id="b8beb-123">Anger namnet på ett virtuellt Azure RemoteApp-nätverk.</span><span class="sxs-lookup"><span data-stu-id="b8beb-123">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8beb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8beb-124">CommonParameters</span></span>
<span data-ttu-id="b8beb-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8beb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8beb-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8beb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8beb-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8beb-127">INPUTS</span></span>

## <span data-ttu-id="b8beb-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8beb-128">OUTPUTS</span></span>

## <span data-ttu-id="b8beb-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8beb-129">NOTES</span></span>

## <span data-ttu-id="b8beb-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8beb-130">RELATED LINKS</span></span>

[<span data-ttu-id="b8beb-131">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="b8beb-131">Get-AzureRemoteAppVpnDevice</span></span>](./Get-AzureRemoteAppVpnDevice.md)


