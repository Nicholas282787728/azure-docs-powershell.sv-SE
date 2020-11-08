---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 913b610bc1d79c7a1792c06b53947fd3bf51151a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088599"
---
# <span data-ttu-id="87d12-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="87d12-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="87d12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87d12-102">SYNOPSIS</span></span>
<span data-ttu-id="87d12-103">Lägg till vanligt namn eller tumavtryck i klustret för användning av klientautentisering.</span><span class="sxs-lookup"><span data-stu-id="87d12-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="87d12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87d12-104">SYNTAX</span></span>

### <span data-ttu-id="87d12-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="87d12-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d12-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="87d12-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d12-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="87d12-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d12-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="87d12-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87d12-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87d12-109">DESCRIPTION</span></span>
<span data-ttu-id="87d12-110">Använd **Add-AzServiceFabricClientCertificate** för att lägga till ett namn och tumavtryck för tumavtryck i klustret, så klienten kan använda det för att verifiera.</span><span class="sxs-lookup"><span data-stu-id="87d12-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="87d12-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87d12-111">EXAMPLES</span></span>

### <span data-ttu-id="87d12-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="87d12-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="87d12-113">Det här kommandot lägger till certifikatet med tumavtrycket ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' i klustret, så klienten kan använda certifikatet som administratör för att kommunicera med klustret.</span><span class="sxs-lookup"><span data-stu-id="87d12-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="87d12-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="87d12-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="87d12-115">Det här kommandot lägger till ett skrivskyddat klient certifikat som är ett vanligt namn är ' Contoso.com ' och utfärdarens tumavtryck är ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' till klustret.</span><span class="sxs-lookup"><span data-stu-id="87d12-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="87d12-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87d12-116">PARAMETERS</span></span>

### <span data-ttu-id="87d12-117">-Admin</span><span class="sxs-lookup"><span data-stu-id="87d12-117">-Admin</span></span>
<span data-ttu-id="87d12-118">Klientens autentiseringstyp</span><span class="sxs-lookup"><span data-stu-id="87d12-118">Client authentication type</span></span>

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

### <span data-ttu-id="87d12-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="87d12-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="87d12-120">Ange tumavtryck för klient certifikat som bara har administratörs behörighet</span><span class="sxs-lookup"><span data-stu-id="87d12-120">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="87d12-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="87d12-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="87d12-122">Ange klientens nätverks namn, utfärdarens tumavtryck och autentiseringstyp</span><span class="sxs-lookup"><span data-stu-id="87d12-122">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="87d12-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="87d12-123">-CommonName</span></span>
<span data-ttu-id="87d12-124">Ange klient certifikatets allmänna namn</span><span class="sxs-lookup"><span data-stu-id="87d12-124">Specify client certificate common name</span></span>

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

### <span data-ttu-id="87d12-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d12-125">-DefaultProfile</span></span>
<span data-ttu-id="87d12-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87d12-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d12-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="87d12-127">-IssuerThumbprint</span></span>
<span data-ttu-id="87d12-128">Ange tumavtryck för klient certifikatets utgivare</span><span class="sxs-lookup"><span data-stu-id="87d12-128">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="87d12-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="87d12-129">-Name</span></span>
<span data-ttu-id="87d12-130">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="87d12-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="87d12-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="87d12-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="87d12-132">Ange tumavtryck för klient certifikat som bara har Skriv behörighet</span><span class="sxs-lookup"><span data-stu-id="87d12-132">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="87d12-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d12-133">-ResourceGroupName</span></span>
<span data-ttu-id="87d12-134">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="87d12-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="87d12-135">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="87d12-135">-Thumbprint</span></span>
<span data-ttu-id="87d12-136">Ange tumavtryck för klient certifikat</span><span class="sxs-lookup"><span data-stu-id="87d12-136">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="87d12-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="87d12-137">-Confirm</span></span>
<span data-ttu-id="87d12-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="87d12-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87d12-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87d12-139">-WhatIf</span></span>
<span data-ttu-id="87d12-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="87d12-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87d12-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="87d12-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87d12-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d12-142">CommonParameters</span></span>
<span data-ttu-id="87d12-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d12-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d12-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87d12-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d12-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87d12-145">INPUTS</span></span>

### <span data-ttu-id="87d12-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87d12-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="87d12-147">System. String</span><span class="sxs-lookup"><span data-stu-id="87d12-147">System.String</span></span>

### <span data-ttu-id="87d12-148">System. string []</span><span class="sxs-lookup"><span data-stu-id="87d12-148">System.String[]</span></span>

### <span data-ttu-id="87d12-149">Microsoft. Azure. commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="87d12-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="87d12-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87d12-150">OUTPUTS</span></span>

### <span data-ttu-id="87d12-151">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="87d12-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="87d12-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87d12-152">NOTES</span></span>

## <span data-ttu-id="87d12-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87d12-153">RELATED LINKS</span></span>

[<span data-ttu-id="87d12-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="87d12-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
