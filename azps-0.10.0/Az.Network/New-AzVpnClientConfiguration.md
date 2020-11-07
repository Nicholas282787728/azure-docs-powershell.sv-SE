---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: caad6363e49d3ac3fe4e591fba860251c0a1d3c0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922082"
---
# <span data-ttu-id="b5e07-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5e07-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="b5e07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5e07-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e07-103">Med det här kommandot kan användarna skapa ett VPN-grupppaket baserat på förkonfigurerade VPN-inställningar på VPN-gatewayen, utöver ytterligare inställningar som användarna kan behöva konfigurera, till exempel. vissa rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="b5e07-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="b5e07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5e07-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5e07-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5e07-105">DESCRIPTION</span></span>
<span data-ttu-id="b5e07-106">då kan användarna skapa ett VPN-grupppaket baserat på förkonfigurerade VPN-inställningar på VPN-gatewayen, samt vissa ytterligare inställningar som användarna kan behöva konfigurera, till exempel. vissa rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="b5e07-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="b5e07-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5e07-107">EXAMPLES</span></span>

### <span data-ttu-id="b5e07-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b5e07-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="b5e07-109">Denna cmdlet används för att skapa en zip-fil för VPN-klienter för "ContosoVirtualNetworkGateway" i ResourceGroup "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="b5e07-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="b5e07-110">Profilen genereras för en förkonfigurerad RADIUS-server som är konfigurerad att använda autentiseringsmetoden "EAPTLS" med VpnProfileRadiusCert-certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="b5e07-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="b5e07-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5e07-111">PARAMETERS</span></span>

### <span data-ttu-id="b5e07-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="b5e07-112">-AuthenticationMethod</span></span>
<span data-ttu-id="b5e07-113">Autentiseringsmetoden kan ta värden EAPMSCHAPv2 eller EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="b5e07-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="b5e07-114">När EAPMSCHAPv2 anges genererar cmdleten ett installations program för klient konfiguration för användar namn/lösen ord som använder EAP-MSCHAPv2 autentiseringsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="b5e07-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="b5e07-115">Om EAPTLS anges genererar cmdleten ett installations program för klient konfiguration för certifikatautentisering som använder EAP-TLS-protokoll.</span><span class="sxs-lookup"><span data-stu-id="b5e07-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="b5e07-116">Alternativet "EapTls" kan användas för både RADIUS-baserad certifikatautentisering och certifikatautentisering som utförs av den virtuella Nätverksgatewayen genom att överföra den betrodda roten.</span><span class="sxs-lookup"><span data-stu-id="b5e07-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="b5e07-117">Cmdleten upptäcker automatiskt vad som är konfigurerat.</span><span class="sxs-lookup"><span data-stu-id="b5e07-117">The cmdlet automatically detects what is configured.</span></span>

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

### <span data-ttu-id="b5e07-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="b5e07-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="b5e07-119">En lista över sökvägar till klient rot certifikat</span><span class="sxs-lookup"><span data-stu-id="b5e07-119">A list of client root certificate paths</span></span>
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

### <span data-ttu-id="b5e07-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e07-120">-DefaultProfile</span></span>
<span data-ttu-id="b5e07-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5e07-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="b5e07-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5e07-122">-Name</span></span>
<span data-ttu-id="b5e07-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="b5e07-123">The resource name.</span></span>

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

### <span data-ttu-id="b5e07-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="b5e07-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="b5e07-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="b5e07-125">ProcessorArchitecture</span></span>

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

### <span data-ttu-id="b5e07-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="b5e07-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="b5e07-127">Sökväg till rot certifikat för RADIUS-server.</span><span class="sxs-lookup"><span data-stu-id="b5e07-127">Radius server root certificate path.</span></span> <span data-ttu-id="b5e07-128">Det här är en obligatorisk parameter som måste anges när EAP-TLS används för RADIUS-identifiering.</span><span class="sxs-lookup"><span data-stu-id="b5e07-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="b5e07-129">Det här är den fullständiga sökvägen till CER-filen som innehåller RADIUS-rotcertifikatet som klienten använder för att validera RADIUS-servern vid verifiering.</span><span class="sxs-lookup"><span data-stu-id="b5e07-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="b5e07-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5e07-130">-ResourceGroupName</span></span>
<span data-ttu-id="b5e07-131">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b5e07-131">The resource group name.</span></span>

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

### <span data-ttu-id="b5e07-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5e07-132">-Confirm</span></span>
<span data-ttu-id="b5e07-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5e07-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5e07-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5e07-134">-WhatIf</span></span>
<span data-ttu-id="b5e07-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5e07-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5e07-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5e07-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5e07-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e07-137">CommonParameters</span></span>
<span data-ttu-id="b5e07-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5e07-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e07-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5e07-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e07-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5e07-140">INPUTS</span></span>

### <span data-ttu-id="b5e07-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b5e07-141">System.String</span></span>
<span data-ttu-id="b5e07-142">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b5e07-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b5e07-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5e07-143">OUTPUTS</span></span>

### <span data-ttu-id="b5e07-144">Microsoft. Azure. commands. Networks. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="b5e07-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="b5e07-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5e07-145">NOTES</span></span>

## <span data-ttu-id="b5e07-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5e07-146">RELATED LINKS</span></span>

