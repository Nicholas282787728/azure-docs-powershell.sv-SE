---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: a2b8d83254c84ee974173611912dd9b21cb7a26d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090452"
---
# <span data-ttu-id="235ea-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="235ea-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="235ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="235ea-102">SYNOPSIS</span></span>
<span data-ttu-id="235ea-103">Återställer principen från en klient organisation i Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="235ea-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="235ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="235ea-104">SYNTAX</span></span>

### <span data-ttu-id="235ea-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="235ea-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="235ea-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="235ea-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="235ea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="235ea-107">DESCRIPTION</span></span>
<span data-ttu-id="235ea-108">Reset-AzAttestationPolicy cmdlet återställer en användardefinierad policy för attestering från en klient organisation i Azure-attestering.</span><span class="sxs-lookup"><span data-stu-id="235ea-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="235ea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="235ea-109">EXAMPLES</span></span>

### <span data-ttu-id="235ea-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="235ea-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="235ea-111">Återställ principen till standardvärdet för *pshtest* för shirt ( *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="235ea-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="235ea-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="235ea-112">PARAMETERS</span></span>

### <span data-ttu-id="235ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="235ea-113">-DefaultProfile</span></span>
<span data-ttu-id="235ea-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="235ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="235ea-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="235ea-115">-Name</span></span>
<span data-ttu-id="235ea-116">Anger ett namn på innehavaren.</span><span class="sxs-lookup"><span data-stu-id="235ea-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="235ea-117">Denna cmdlet återställer policyn för attestering för den klient organisation som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="235ea-117">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="235ea-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="235ea-118">-PassThru</span></span>
<span data-ttu-id="235ea-119">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="235ea-119">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="235ea-120">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="235ea-120">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="235ea-121">-Princip</span><span class="sxs-lookup"><span data-stu-id="235ea-121">-Policy</span></span>
<span data-ttu-id="235ea-122">Anger den JSON Web token som beskriver princip dokumentet som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="235ea-122">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="235ea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="235ea-123">-ResourceGroupName</span></span>
<span data-ttu-id="235ea-124">Anger namnet på en attesterings leverantörs resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="235ea-124">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="235ea-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="235ea-125">-ResourceId</span></span>
<span data-ttu-id="235ea-126">Anger ResourceID för en attesterings leverantör.</span><span class="sxs-lookup"><span data-stu-id="235ea-126">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="235ea-127">-Shirt (</span><span class="sxs-lookup"><span data-stu-id="235ea-127">-Tee</span></span>
<span data-ttu-id="235ea-128">Anger en typ av körnings miljö.</span><span class="sxs-lookup"><span data-stu-id="235ea-128">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="235ea-129">Vi har stöd för fyra typer av miljöer: SgxEnclave, OpenEnclave, CyResComponent och VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="235ea-129">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="235ea-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="235ea-130">-Confirm</span></span>
<span data-ttu-id="235ea-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="235ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="235ea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="235ea-132">-WhatIf</span></span>
<span data-ttu-id="235ea-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="235ea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="235ea-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="235ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="235ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="235ea-135">CommonParameters</span></span>
<span data-ttu-id="235ea-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="235ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="235ea-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="235ea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="235ea-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="235ea-138">INPUTS</span></span>

### <span data-ttu-id="235ea-139">System. String</span><span class="sxs-lookup"><span data-stu-id="235ea-139">System.String</span></span>

## <span data-ttu-id="235ea-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="235ea-140">OUTPUTS</span></span>

### <span data-ttu-id="235ea-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="235ea-141">System.Boolean</span></span>

## <span data-ttu-id="235ea-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="235ea-142">NOTES</span></span>

## <span data-ttu-id="235ea-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="235ea-143">RELATED LINKS</span></span>
