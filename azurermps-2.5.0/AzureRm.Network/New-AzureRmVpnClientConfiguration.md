---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientconfiguration
schema: 2.0.0
ms.openlocfilehash: d49078e18b6082473c398c9f4aa7ac01f41909ca
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930534"
---
# <span data-ttu-id="e901b-101">New-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="e901b-101">New-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="e901b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e901b-102">SYNOPSIS</span></span>
<span data-ttu-id="e901b-103">Med det här kommandot kan användarna skapa ett VPN-grupppaket baserat på förkonfigurerade VPN-inställningar på VPN-gatewayen, utöver ytterligare inställningar som användarna kan behöva konfigurera, till exempel. vissa rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="e901b-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e901b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e901b-104">SYNTAX</span></span>

```
New-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e901b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e901b-105">DESCRIPTION</span></span>
<span data-ttu-id="e901b-106">då kan användarna skapa ett VPN-grupppaket baserat på förkonfigurerade VPN-inställningar på VPN-gatewayen, samt vissa ytterligare inställningar som användarna kan behöva konfigurera, till exempel. vissa rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="e901b-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="e901b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e901b-107">EXAMPLES</span></span>

### <span data-ttu-id="e901b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e901b-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="e901b-109">Denna cmdlet används för att skapa en zip-fil för VPN-klienter för "ContosoVirtualNetworkGateway" i ResourceGroup "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="e901b-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="e901b-110">Profilen genereras för en förkonfigurerad RADIUS-server som är konfigurerad att använda autentiseringsmetoden "EAPTLS" med VpnProfileRadiusCert-certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="e901b-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="e901b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e901b-111">PARAMETERS</span></span>

### <span data-ttu-id="e901b-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="e901b-112">-AuthenticationMethod</span></span>
<span data-ttu-id="e901b-113">Autentiseringsmetoden kan ta värden EAPMSCHAPv2 eller EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="e901b-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="e901b-114">När EAPMSCHAPv2 anges genererar cmdleten ett installations program för klient konfiguration för användar namn/lösen ord som använder EAP-MSCHAPv2 autentiseringsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="e901b-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="e901b-115">Om EAPTLS anges genererar cmdleten ett installations program för klient konfiguration för certifikatautentisering som använder EAP-TLS-protokoll.</span><span class="sxs-lookup"><span data-stu-id="e901b-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="e901b-116">Alternativet "EapTls" kan användas för både RADIUS-baserad certifikatautentisering och certifikatautentisering som utförs av den virtuella Nätverksgatewayen genom att överföra den betrodda roten.</span><span class="sxs-lookup"><span data-stu-id="e901b-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="e901b-117">Cmdleten upptäcker automatiskt vad som är konfigurerat.</span><span class="sxs-lookup"><span data-stu-id="e901b-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e901b-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="e901b-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="e901b-119">En lista över sökvägar till klient rot certifikat</span><span class="sxs-lookup"><span data-stu-id="e901b-119">A list of client root certificate paths</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e901b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e901b-120">-DefaultProfile</span></span>
<span data-ttu-id="e901b-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e901b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e901b-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e901b-122">-Name</span></span>
<span data-ttu-id="e901b-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e901b-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e901b-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="e901b-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="e901b-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="e901b-125">ProcessorArchitecture</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e901b-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="e901b-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="e901b-127">Sökväg till rot certifikat för RADIUS-server.</span><span class="sxs-lookup"><span data-stu-id="e901b-127">Radius server root certificate path.</span></span> <span data-ttu-id="e901b-128">Det här är en obligatorisk parameter som måste anges när EAP-TLS används för RADIUS-identifiering.</span><span class="sxs-lookup"><span data-stu-id="e901b-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="e901b-129">Det här är den fullständiga sökvägen till CER-filen som innehåller RADIUS-rotcertifikatet som klienten använder för att validera RADIUS-servern vid verifiering.</span><span class="sxs-lookup"><span data-stu-id="e901b-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e901b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e901b-130">-ResourceGroupName</span></span>
<span data-ttu-id="e901b-131">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e901b-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e901b-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e901b-132">-Confirm</span></span>
<span data-ttu-id="e901b-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e901b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e901b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e901b-134">-WhatIf</span></span>
<span data-ttu-id="e901b-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e901b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e901b-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e901b-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e901b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e901b-137">CommonParameters</span></span>
<span data-ttu-id="e901b-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e901b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e901b-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e901b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e901b-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e901b-140">INPUTS</span></span>

### <span data-ttu-id="e901b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e901b-141">System.String</span></span>
<span data-ttu-id="e901b-142">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e901b-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e901b-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e901b-143">OUTPUTS</span></span>

### <span data-ttu-id="e901b-144">Microsoft. Azure. commands. Networks. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="e901b-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="e901b-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e901b-145">NOTES</span></span>

## <span data-ttu-id="e901b-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e901b-146">RELATED LINKS</span></span>

