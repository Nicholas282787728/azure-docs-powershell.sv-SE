---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: c7a88cad933781b00e720c273be467966991cebf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398827"
---
# <span data-ttu-id="25877-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="25877-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="25877-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25877-102">SYNOPSIS</span></span>
<span data-ttu-id="25877-103">Ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.</span><span class="sxs-lookup"><span data-stu-id="25877-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="25877-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25877-104">SYNTAX</span></span>

### <span data-ttu-id="25877-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="25877-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25877-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="25877-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25877-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="25877-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25877-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="25877-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25877-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25877-109">DESCRIPTION</span></span>
<span data-ttu-id="25877-110">Använd **Remove-AzServiceFabricClientCertificate** om du vill ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.</span><span class="sxs-lookup"><span data-stu-id="25877-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="25877-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25877-111">EXAMPLES</span></span>

### <span data-ttu-id="25877-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25877-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="25877-113">Det här kommandot tar bort klient certifikatet med tumavtrycket ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' från klustret.</span><span class="sxs-lookup"><span data-stu-id="25877-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="25877-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25877-114">PARAMETERS</span></span>

### <span data-ttu-id="25877-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="25877-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="25877-116">Ange tumavtryck för klient certifikat som bara har administratörs behörighet</span><span class="sxs-lookup"><span data-stu-id="25877-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="25877-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="25877-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="25877-118">Ange klientens nätverks namn, utfärdarens tumavtryck och autentiseringstyp</span><span class="sxs-lookup"><span data-stu-id="25877-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="25877-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="25877-119">-CommonName</span></span>
<span data-ttu-id="25877-120">Ange klient certifikatets allmänna namn</span><span class="sxs-lookup"><span data-stu-id="25877-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="25877-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25877-121">-DefaultProfile</span></span>
<span data-ttu-id="25877-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25877-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25877-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="25877-123">-IssuerThumbprint</span></span>
<span data-ttu-id="25877-124">Ange tumavtryck för klient certifikatets utgivare</span><span class="sxs-lookup"><span data-stu-id="25877-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="25877-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="25877-125">-Name</span></span>
<span data-ttu-id="25877-126">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="25877-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="25877-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="25877-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="25877-128">Ange tumavtryck för klient certifikat som bara har Skriv behörighet</span><span class="sxs-lookup"><span data-stu-id="25877-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="25877-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25877-129">-ResourceGroupName</span></span>
<span data-ttu-id="25877-130">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="25877-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="25877-131">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="25877-131">-Thumbprint</span></span>
<span data-ttu-id="25877-132">Ange tumavtryck för klient certifikat</span><span class="sxs-lookup"><span data-stu-id="25877-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="25877-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="25877-133">-Confirm</span></span>
<span data-ttu-id="25877-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="25877-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25877-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25877-135">-WhatIf</span></span>
<span data-ttu-id="25877-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="25877-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25877-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="25877-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25877-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25877-138">CommonParameters</span></span>
<span data-ttu-id="25877-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25877-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25877-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25877-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25877-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25877-141">INPUTS</span></span>

### <span data-ttu-id="25877-142">System. String</span><span class="sxs-lookup"><span data-stu-id="25877-142">System.String</span></span>

### <span data-ttu-id="25877-143">System. string []</span><span class="sxs-lookup"><span data-stu-id="25877-143">System.String[]</span></span>

### <span data-ttu-id="25877-144">Microsoft. Azure. commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="25877-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="25877-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25877-145">OUTPUTS</span></span>

### <span data-ttu-id="25877-146">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="25877-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="25877-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25877-147">NOTES</span></span>

## <span data-ttu-id="25877-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25877-148">RELATED LINKS</span></span>

[<span data-ttu-id="25877-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="25877-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
