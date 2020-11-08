---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093197"
---
# <span data-ttu-id="37c9c-101">Reset-AzureRemoteAppVpnSharedKey</span><span class="sxs-lookup"><span data-stu-id="37c9c-101">Reset-AzureRemoteAppVpnSharedKey</span></span>

## <span data-ttu-id="37c9c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="37c9c-103">Återställer den delade Azure RemoteApp VPN-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="37c9c-103">Resets the Azure RemoteApp VPN shared key.</span></span>

## <span data-ttu-id="37c9c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37c9c-104">SYNTAX</span></span>

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37c9c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="37c9c-106">Cmdleten **Reset-AzureRemoteAppVpnSharedKey** återställer Azure RemoteApp-den virtuella privata nätverks nycklar (VPN).</span><span class="sxs-lookup"><span data-stu-id="37c9c-106">The **Reset-AzureRemoteAppVpnSharedKey** cmdlet resets the Azure RemoteApp virtual private network (VPN) shared key.</span></span>

## <span data-ttu-id="37c9c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37c9c-107">EXAMPLES</span></span>

### <span data-ttu-id="37c9c-108">Exempel 1: Återställ den delade knappen i ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="37c9c-108">Example 1: Reset the shared key on a virtual network</span></span>
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

<span data-ttu-id="37c9c-109">Det här kommandot återställer den delade knappen på det virtuella nätverket med namnet ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="37c9c-109">This command resets the shared key on the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="37c9c-110">VPN-anslutningen till det lokala nätverket är offline tills den nya delade knappen är konfigurerad på VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="37c9c-110">The VPN connection to the on-premises network remains offline until the new shared key is configured on the VPN device.</span></span>
<span data-ttu-id="37c9c-111">Konfigurera VPN-enheten genom att använda cmdleten **Get-AzureRemoteAppVpnDeviceConfigScript** för att hämta rätt skript eller konfigurations fil för din VPN-enhet och sedan Ladda skriptet eller konfigurations filen till VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="37c9c-111">To configure the VPN device, use the **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet to retrieve the correct script or configuration file for your VPN device, then load that script or configuration file onto the VPN device.</span></span>

## <span data-ttu-id="37c9c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37c9c-112">PARAMETERS</span></span>

### <span data-ttu-id="37c9c-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="37c9c-113">-Profile</span></span>
<span data-ttu-id="37c9c-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="37c9c-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="37c9c-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="37c9c-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37c9c-116">-VNetName</span><span class="sxs-lookup"><span data-stu-id="37c9c-116">-VNetName</span></span>
<span data-ttu-id="37c9c-117">Anger namnet på det virtuella Azure RemoteApp-nätverket.</span><span class="sxs-lookup"><span data-stu-id="37c9c-117">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="37c9c-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="37c9c-118">-Confirm</span></span>
<span data-ttu-id="37c9c-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37c9c-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c9c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c9c-120">-WhatIf</span></span>
<span data-ttu-id="37c9c-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="37c9c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37c9c-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="37c9c-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c9c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c9c-123">CommonParameters</span></span>
<span data-ttu-id="37c9c-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c9c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c9c-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37c9c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c9c-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37c9c-126">INPUTS</span></span>

## <span data-ttu-id="37c9c-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37c9c-127">OUTPUTS</span></span>

### <span data-ttu-id="37c9c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="37c9c-128">System.String</span></span>

## <span data-ttu-id="37c9c-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37c9c-129">NOTES</span></span>

## <span data-ttu-id="37c9c-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37c9c-130">RELATED LINKS</span></span>

[<span data-ttu-id="37c9c-131">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="37c9c-131">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="37c9c-132">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="37c9c-132">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


