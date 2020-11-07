---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: e508afc5ab66a3e2aec49131bf2c8bf0e9d31259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755583"
---
# <span data-ttu-id="b77fe-101">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b77fe-101">Remove-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="b77fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b77fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b77fe-103">Ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.</span><span class="sxs-lookup"><span data-stu-id="b77fe-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b77fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b77fe-104">SYNTAX</span></span>

### <span data-ttu-id="b77fe-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="b77fe-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b77fe-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="b77fe-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b77fe-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="b77fe-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b77fe-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="b77fe-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b77fe-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b77fe-109">DESCRIPTION</span></span>
<span data-ttu-id="b77fe-110">Använd **Remove-AzureRmServiceFabricClientCertificate** om du vill ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.</span><span class="sxs-lookup"><span data-stu-id="b77fe-110">Use **Remove-AzureRmServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="b77fe-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b77fe-111">EXAMPLES</span></span>

### <span data-ttu-id="b77fe-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b77fe-112">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="b77fe-113">Det här kommandot tar bort klient certifikatet med tumavtrycket ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' från klustret.</span><span class="sxs-lookup"><span data-stu-id="b77fe-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="b77fe-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b77fe-114">PARAMETERS</span></span>

### <span data-ttu-id="b77fe-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="b77fe-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="b77fe-116">Ange tumavtryck för klient certifikat som bara har administratörs behörighet.</span><span class="sxs-lookup"><span data-stu-id="b77fe-116">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b77fe-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="b77fe-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="b77fe-118">Ange klientens allmänna namn, utfärdarens tumavtryck och autentiseringstyp.</span><span class="sxs-lookup"><span data-stu-id="b77fe-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b77fe-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="b77fe-119">-CommonName</span></span>
<span data-ttu-id="b77fe-120">Ange klient certifikatets allmänna namn.</span><span class="sxs-lookup"><span data-stu-id="b77fe-120">Specify client certificate common name.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b77fe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77fe-121">-DefaultProfile</span></span>
<span data-ttu-id="b77fe-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b77fe-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b77fe-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="b77fe-123">-IssuerThumbprint</span></span>
<span data-ttu-id="b77fe-124">Ange tumavtryck för klient certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="b77fe-124">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b77fe-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="b77fe-125">-Name</span></span>
<span data-ttu-id="b77fe-126">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="b77fe-126">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b77fe-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="b77fe-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="b77fe-128">Ange tumavtryck för klient certifikat som har Skriv behörighet.</span><span class="sxs-lookup"><span data-stu-id="b77fe-128">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b77fe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b77fe-129">-ResourceGroupName</span></span>
<span data-ttu-id="b77fe-130">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b77fe-130">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b77fe-131">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="b77fe-131">-Thumbprint</span></span>
<span data-ttu-id="b77fe-132">Ange tumavtryck för klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="b77fe-132">Specify client certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b77fe-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b77fe-133">-Confirm</span></span>
<span data-ttu-id="b77fe-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b77fe-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b77fe-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b77fe-135">-WhatIf</span></span>
<span data-ttu-id="b77fe-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b77fe-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b77fe-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b77fe-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b77fe-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77fe-138">CommonParameters</span></span>
<span data-ttu-id="b77fe-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b77fe-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77fe-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b77fe-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77fe-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b77fe-141">INPUTS</span></span>

### <span data-ttu-id="b77fe-142">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b77fe-142">System.Collections.Hashtable</span></span>
<span data-ttu-id="b77fe-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b77fe-143">System.String</span></span>

<span data-ttu-id="b77fe-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b77fe-144">System.Boolean</span></span>

## <span data-ttu-id="b77fe-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b77fe-145">OUTPUTS</span></span>

### <span data-ttu-id="b77fe-146">Microsoft. Azure. commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="b77fe-146">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="b77fe-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b77fe-147">NOTES</span></span>

## <span data-ttu-id="b77fe-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b77fe-148">RELATED LINKS</span></span>

[<span data-ttu-id="b77fe-149">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b77fe-149">Add-AzureRmServiceFabricClientCertificate</span></span>](./Add-AzureRmServiceFabricClientCertificate.md)
