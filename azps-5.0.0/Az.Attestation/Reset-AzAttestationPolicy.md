---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321892"
---
# <span data-ttu-id="f2eb7-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="f2eb7-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="f2eb7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="f2eb7-103">Återställer principen från en klient organisation i Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="f2eb7-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="f2eb7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2eb7-104">SYNTAX</span></span>

### <span data-ttu-id="f2eb7-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2eb7-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2eb7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2eb7-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2eb7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2eb7-107">DESCRIPTION</span></span>
<span data-ttu-id="f2eb7-108">Reset-AzAttestationPolicy cmdlet återställer en användardefinierad policy för attestering från en klient organisation i Azure-attestering.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f2eb7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2eb7-109">EXAMPLES</span></span>

### <span data-ttu-id="f2eb7-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f2eb7-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="f2eb7-111">Återställ principen till standardvärdet för *pshtest* för shirt ( *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="f2eb7-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f2eb7-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="f2eb7-113">Om *pshtest* för attestering är konfigurerad för att använda isolerad förtroende modell återställer du principen till standardvärdet för shirt (typ *SgxEnclave* genom att inkludera en signerad princip.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="f2eb7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2eb7-114">PARAMETERS</span></span>

### <span data-ttu-id="f2eb7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2eb7-115">-DefaultProfile</span></span>
<span data-ttu-id="f2eb7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2eb7-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2eb7-117">-Name</span></span>
<span data-ttu-id="f2eb7-118">Anger ett namn på innehavaren.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="f2eb7-119">Denna cmdlet återställer policyn för attestering för den klient organisation som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2eb7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2eb7-120">-PassThru</span></span>
<span data-ttu-id="f2eb7-121">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f2eb7-122">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f2eb7-123">-Princip</span><span class="sxs-lookup"><span data-stu-id="f2eb7-123">-Policy</span></span>
<span data-ttu-id="f2eb7-124">Anger den JSON Web token som beskriver princip dokumentet som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="f2eb7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2eb7-125">-ResourceGroupName</span></span>
<span data-ttu-id="f2eb7-126">Anger namnet på en attesterings leverantörs resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="f2eb7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2eb7-127">-ResourceId</span></span>
<span data-ttu-id="f2eb7-128">Anger ResourceID för en attesterings leverantör.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="f2eb7-129">-Shirt (</span><span class="sxs-lookup"><span data-stu-id="f2eb7-129">-Tee</span></span>
<span data-ttu-id="f2eb7-130">Anger en typ av körnings miljö.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="f2eb7-131">Vi har stöd för fyra typer av miljöer: SgxEnclave, OpenEnclave, CyResComponent och VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="f2eb7-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2eb7-132">-Confirm</span></span>
<span data-ttu-id="f2eb7-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2eb7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2eb7-134">-WhatIf</span></span>
<span data-ttu-id="f2eb7-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2eb7-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2eb7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2eb7-137">CommonParameters</span></span>
<span data-ttu-id="f2eb7-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2eb7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2eb7-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2eb7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2eb7-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2eb7-140">INPUTS</span></span>

### <span data-ttu-id="f2eb7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f2eb7-141">System.String</span></span>

## <span data-ttu-id="f2eb7-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2eb7-142">OUTPUTS</span></span>

### <span data-ttu-id="f2eb7-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2eb7-143">System.Boolean</span></span>

## <span data-ttu-id="f2eb7-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2eb7-144">NOTES</span></span>

## <span data-ttu-id="f2eb7-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2eb7-145">RELATED LINKS</span></span>