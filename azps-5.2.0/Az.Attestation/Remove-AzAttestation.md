---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406651"
---
# <span data-ttu-id="524ed-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="524ed-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="524ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="524ed-102">SYNOPSIS</span></span>
<span data-ttu-id="524ed-103">Tar bort en attestering.</span><span class="sxs-lookup"><span data-stu-id="524ed-103">Deletes an attestation.</span></span>

## <span data-ttu-id="524ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="524ed-104">SYNTAX</span></span>

### <span data-ttu-id="524ed-105">ByAvailableAttestation (standard)</span><span class="sxs-lookup"><span data-stu-id="524ed-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="524ed-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="524ed-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="524ed-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="524ed-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="524ed-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="524ed-108">DESCRIPTION</span></span>
<span data-ttu-id="524ed-109">Remove-AzAttestation-cmdleten tar bort angiven attestering.</span><span class="sxs-lookup"><span data-stu-id="524ed-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="524ed-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="524ed-110">EXAMPLES</span></span>

### <span data-ttu-id="524ed-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="524ed-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="524ed-112">Ta bort Attesteringsservern som heter *pshtest3* i resurs gruppen med namnet *PSH-test-RG* från det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="524ed-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="524ed-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="524ed-113">PARAMETERS</span></span>

### <span data-ttu-id="524ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="524ed-114">-DefaultProfile</span></span>
<span data-ttu-id="524ed-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="524ed-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="524ed-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="524ed-116">-InputObject</span></span>
<span data-ttu-id="524ed-117">Attesterings objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="524ed-117">Attestation object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Attestation.Models.PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="524ed-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="524ed-118">-Name</span></span>
<span data-ttu-id="524ed-119">Anger namnet på den attestering som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="524ed-119">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="524ed-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="524ed-120">-PassThru</span></span>
<span data-ttu-id="524ed-121">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="524ed-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="524ed-122">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="524ed-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="524ed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="524ed-123">-ResourceGroupName</span></span>
<span data-ttu-id="524ed-124">Anger namnet på resurs gruppen för Azure-attestering som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="524ed-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="524ed-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="524ed-125">-ResourceId</span></span>
<span data-ttu-id="524ed-126">Resurs-ID för attestering.</span><span class="sxs-lookup"><span data-stu-id="524ed-126">Attestation Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="524ed-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="524ed-127">-Confirm</span></span>
<span data-ttu-id="524ed-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="524ed-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="524ed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="524ed-129">-WhatIf</span></span>
<span data-ttu-id="524ed-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="524ed-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="524ed-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="524ed-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="524ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="524ed-132">CommonParameters</span></span>
<span data-ttu-id="524ed-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="524ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="524ed-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="524ed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="524ed-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="524ed-135">INPUTS</span></span>

### <span data-ttu-id="524ed-136">System. String</span><span class="sxs-lookup"><span data-stu-id="524ed-136">System.String</span></span>

### <span data-ttu-id="524ed-137">Microsoft. Azure. commands. attestering. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="524ed-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="524ed-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="524ed-138">OUTPUTS</span></span>

### <span data-ttu-id="524ed-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="524ed-139">System.Boolean</span></span>

## <span data-ttu-id="524ed-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="524ed-140">NOTES</span></span>

## <span data-ttu-id="524ed-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="524ed-141">RELATED LINKS</span></span>
