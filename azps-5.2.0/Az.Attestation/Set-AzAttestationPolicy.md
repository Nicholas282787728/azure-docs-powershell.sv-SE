---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406640"
---
# <span data-ttu-id="5c620-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="5c620-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="5c620-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c620-102">SYNOPSIS</span></span>
<span data-ttu-id="5c620-103">Ställer in principen från en klient organisation i Azure Attestationn.</span><span class="sxs-lookup"><span data-stu-id="5c620-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="5c620-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c620-104">SYNTAX</span></span>

### <span data-ttu-id="5c620-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c620-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c620-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c620-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c620-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c620-107">DESCRIPTION</span></span>
<span data-ttu-id="5c620-108">Den Set-AzAttestationPolicy cmdleten ställer in policyn från en klient organisation i Azure-attestering.</span><span class="sxs-lookup"><span data-stu-id="5c620-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="5c620-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c620-109">EXAMPLES</span></span>

### <span data-ttu-id="5c620-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5c620-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="5c620-111">Anger den användardefinierade principen för shirt (typ *SgxEnclave* för attesteringsservern *pshtest* med ett text policy format (standard).</span><span class="sxs-lookup"><span data-stu-id="5c620-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="5c620-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5c620-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="5c620-113">Anger den användardefinierade principen för shirt (typ *SgxEnclave* för attesteringsservern *PSHTEST* med ett JWT-princip-format.</span><span class="sxs-lookup"><span data-stu-id="5c620-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="5c620-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c620-114">PARAMETERS</span></span>

### <span data-ttu-id="5c620-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c620-115">-DefaultProfile</span></span>
<span data-ttu-id="5c620-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c620-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c620-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c620-117">-Name</span></span>
<span data-ttu-id="5c620-118">Anger ett namn på innehavaren.</span><span class="sxs-lookup"><span data-stu-id="5c620-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="5c620-119">Den här cmdleten ställer in policyn för attestering för den klient organisation som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5c620-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="5c620-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c620-120">-PassThru</span></span>
<span data-ttu-id="5c620-121">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="5c620-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5c620-122">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="5c620-122">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c620-123">-Princip</span><span class="sxs-lookup"><span data-stu-id="5c620-123">-Policy</span></span>
<span data-ttu-id="5c620-124">Anger det princip dokument som ska ställas in.</span><span class="sxs-lookup"><span data-stu-id="5c620-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="5c620-125">Princip formatet kan antingen vara text eller JSON Web token (JWT).</span><span class="sxs-lookup"><span data-stu-id="5c620-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="5c620-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="5c620-126">-PolicyFormat</span></span>
<span data-ttu-id="5c620-127">Anger formatet för principen, antingen text eller JWT (JSON Web token).</span><span class="sxs-lookup"><span data-stu-id="5c620-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="5c620-128">Standard princip formatet är text.</span><span class="sxs-lookup"><span data-stu-id="5c620-128">The default policy format is Text.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c620-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c620-129">-ResourceGroupName</span></span>
<span data-ttu-id="5c620-130">Anger namnet på en attesterings leverantörs resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5c620-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="5c620-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c620-131">-ResourceId</span></span>
<span data-ttu-id="5c620-132">Anger ResourceID för en attesterings leverantör.</span><span class="sxs-lookup"><span data-stu-id="5c620-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="5c620-133">-Shirt (</span><span class="sxs-lookup"><span data-stu-id="5c620-133">-Tee</span></span>
<span data-ttu-id="5c620-134">Anger en typ av körnings miljö.</span><span class="sxs-lookup"><span data-stu-id="5c620-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="5c620-135">Det finns fyra typer av miljöer: SgxEnclave, OpenEnclave, CyResComponent och VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="5c620-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="5c620-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5c620-136">-Confirm</span></span>
<span data-ttu-id="5c620-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5c620-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c620-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c620-138">-WhatIf</span></span>
<span data-ttu-id="5c620-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5c620-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c620-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5c620-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c620-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c620-141">CommonParameters</span></span>
<span data-ttu-id="5c620-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c620-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c620-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c620-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c620-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c620-144">INPUTS</span></span>

### <span data-ttu-id="5c620-145">System. String</span><span class="sxs-lookup"><span data-stu-id="5c620-145">System.String</span></span>

## <span data-ttu-id="5c620-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c620-146">OUTPUTS</span></span>

### <span data-ttu-id="5c620-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5c620-147">System.String</span></span>

## <span data-ttu-id="5c620-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c620-148">NOTES</span></span>

## <span data-ttu-id="5c620-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c620-149">RELATED LINKS</span></span>
