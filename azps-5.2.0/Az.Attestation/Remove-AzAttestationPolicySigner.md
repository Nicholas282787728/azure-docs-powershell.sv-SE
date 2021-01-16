---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: fdd62a78b9d75ef222dc9f41f2c791afadfad9b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406659"
---
# <span data-ttu-id="cde80-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="cde80-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="cde80-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cde80-102">SYNOPSIS</span></span>
<span data-ttu-id="cde80-103">Tar bort en betrodd princips undertecknare för en innehavare i Azure-attestering.</span><span class="sxs-lookup"><span data-stu-id="cde80-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="cde80-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cde80-104">SYNTAX</span></span>

### <span data-ttu-id="cde80-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cde80-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cde80-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cde80-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cde80-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cde80-107">DESCRIPTION</span></span>
<span data-ttu-id="cde80-108">Remove-AzAttestationPolicySigner-cmdleten tar bort en betrodd princips undertecknare för en innehavare i Azure-attestering.</span><span class="sxs-lookup"><span data-stu-id="cde80-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="cde80-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cde80-109">EXAMPLES</span></span>

### <span data-ttu-id="cde80-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cde80-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="cde80-111">Ta bort en betrodd undertecknare för Attesteringsservern med namnet *pshtest*.</span><span class="sxs-lookup"><span data-stu-id="cde80-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="cde80-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cde80-112">PARAMETERS</span></span>

### <span data-ttu-id="cde80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde80-113">-DefaultProfile</span></span>
<span data-ttu-id="cde80-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cde80-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cde80-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="cde80-115">-Name</span></span>
<span data-ttu-id="cde80-116">Anger namnet på en attesterings leverantör.</span><span class="sxs-lookup"><span data-stu-id="cde80-116">Specifies the name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cde80-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cde80-117">-ResourceGroupName</span></span>
<span data-ttu-id="cde80-118">Anger namnet på en attesterings leverantörs resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cde80-118">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cde80-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cde80-119">-ResourceId</span></span>
<span data-ttu-id="cde80-120">Anger ResourceID för en attesterings leverantör.</span><span class="sxs-lookup"><span data-stu-id="cde80-120">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cde80-121">-Undertecknare</span><span class="sxs-lookup"><span data-stu-id="cde80-121">-Signer</span></span>
<span data-ttu-id="cde80-122">Anger den RFC7519 JSON Web token som innehåller ett anspråk med namnet "Maa-policyCertificate" vars värde är en RFC7517 JSON-webbnyckel som innehåller en betrodd signerings nyckel som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="cde80-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="cde80-123">RFC7519 JWT måste vara signerat med en av de befintliga betrodda signerings nycklarna.</span><span class="sxs-lookup"><span data-stu-id="cde80-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde80-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cde80-124">-Confirm</span></span>
<span data-ttu-id="cde80-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cde80-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cde80-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cde80-126">-WhatIf</span></span>
<span data-ttu-id="cde80-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cde80-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cde80-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cde80-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cde80-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde80-129">CommonParameters</span></span>
<span data-ttu-id="cde80-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cde80-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde80-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cde80-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde80-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cde80-132">INPUTS</span></span>

### <span data-ttu-id="cde80-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cde80-133">System.String</span></span>

## <span data-ttu-id="cde80-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cde80-134">OUTPUTS</span></span>

### <span data-ttu-id="cde80-135">Microsoft. Azure. commands. attestering. Models. PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="cde80-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="cde80-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cde80-136">NOTES</span></span>

## <span data-ttu-id="cde80-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cde80-137">RELATED LINKS</span></span>
