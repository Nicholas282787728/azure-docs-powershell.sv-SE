---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: 37db0181ea135a0cdb00cddc0a18780fe9fe2d7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757452"
---
# <span data-ttu-id="261a4-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="261a4-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="261a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="261a4-102">SYNOPSIS</span></span>
<span data-ttu-id="261a4-103">Lägg till vanligt namn eller tumavtryck i klustret för användning av klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="261a4-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="261a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="261a4-104">SYNTAX</span></span>

### <span data-ttu-id="261a4-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="261a4-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261a4-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="261a4-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261a4-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="261a4-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261a4-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="261a4-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="261a4-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="261a4-109">DESCRIPTION</span></span>
<span data-ttu-id="261a4-110">Använd **Add-AzureRmServiceFabricClientCertificate** för att lägga till ett namn och tumavtryck för tumavtryck i klustret, så klienten kan använda det för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="261a4-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="261a4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="261a4-111">EXAMPLES</span></span>

### <span data-ttu-id="261a4-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="261a4-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -IsAdmin
```

<span data-ttu-id="261a4-113">Det här kommandot lägger till certifikatet med tumavtrycket ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' i klustret, så klienten kan använda certifikatet som administratör för att kommunicera med klustret.</span><span class="sxs-lookup"><span data-stu-id="261a4-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="261a4-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="261a4-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="261a4-115">Det här kommandot lägger till ett skrivskyddat klient certifikat som är ett vanligt namn är ' Contoso.com ' och utfärdarens tumavtryck är ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' till klustret.</span><span class="sxs-lookup"><span data-stu-id="261a4-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="261a4-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="261a4-116">PARAMETERS</span></span>

### <span data-ttu-id="261a4-117">-Admin</span><span class="sxs-lookup"><span data-stu-id="261a4-117">-Admin</span></span>
<span data-ttu-id="261a4-118">Typ av klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="261a4-118">Client authentication type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="261a4-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="261a4-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="261a4-120">Ange tumavtryck för klient certifikat som bara har administratörs behörighet.</span><span class="sxs-lookup"><span data-stu-id="261a4-120">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="261a4-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="261a4-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="261a4-122">Ange klientens allmänna namn, utfärdarens tumavtryck och autentiseringstyp.</span><span class="sxs-lookup"><span data-stu-id="261a4-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="261a4-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="261a4-123">-CommonName</span></span>
<span data-ttu-id="261a4-124">Ange klient certifikatets allmänna namn.</span><span class="sxs-lookup"><span data-stu-id="261a4-124">Specify client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="261a4-125">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="261a4-125">-IssuerThumbprint</span></span>
<span data-ttu-id="261a4-126">Ange tumavtryck för klient certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="261a4-126">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="261a4-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="261a4-127">-Name</span></span>
<span data-ttu-id="261a4-128">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="261a4-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a4-129">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="261a4-129">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="261a4-130">Ange tumavtryck för klient certifikat som har Skriv behörighet.</span><span class="sxs-lookup"><span data-stu-id="261a4-130">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="261a4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="261a4-131">-ResourceGroupName</span></span>
<span data-ttu-id="261a4-132">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="261a4-132">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261a4-133">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="261a4-133">-Thumbprint</span></span>
<span data-ttu-id="261a4-134">Ange tumavtryck för klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="261a4-134">Specify client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="261a4-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="261a4-135">-Confirm</span></span>
<span data-ttu-id="261a4-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="261a4-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261a4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="261a4-137">-WhatIf</span></span>
<span data-ttu-id="261a4-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="261a4-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="261a4-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="261a4-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261a4-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="261a4-140">-DefaultProfile</span></span>
<span data-ttu-id="261a4-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="261a4-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261a4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="261a4-142">CommonParameters</span></span>
<span data-ttu-id="261a4-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="261a4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="261a4-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="261a4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="261a4-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="261a4-145">INPUTS</span></span>

### <span data-ttu-id="261a4-146">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="261a4-146">System.Collections.Hashtable</span></span>
<span data-ttu-id="261a4-147">System. String</span><span class="sxs-lookup"><span data-stu-id="261a4-147">System.String</span></span>

<span data-ttu-id="261a4-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="261a4-148">System.Boolean</span></span>

## <span data-ttu-id="261a4-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="261a4-149">OUTPUTS</span></span>

### <span data-ttu-id="261a4-150">Microsoft. Azure. commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="261a4-150">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="261a4-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="261a4-151">NOTES</span></span>

## <span data-ttu-id="261a4-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="261a4-152">RELATED LINKS</span></span>

[<span data-ttu-id="261a4-153">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="261a4-153">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
