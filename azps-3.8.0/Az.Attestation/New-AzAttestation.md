---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090464"
---
# <span data-ttu-id="4daf0-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="4daf0-101">New-AzAttestation</span></span>

## <span data-ttu-id="4daf0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4daf0-102">SYNOPSIS</span></span>
<span data-ttu-id="4daf0-103">Skapar en attestering</span><span class="sxs-lookup"><span data-stu-id="4daf0-103">Creates an attestation</span></span>

## <span data-ttu-id="4daf0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4daf0-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4daf0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4daf0-105">DESCRIPTION</span></span>
<span data-ttu-id="4daf0-106">New-AzAttestation cmdlet skapar en attestering i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4daf0-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="4daf0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4daf0-107">EXAMPLES</span></span>

### <span data-ttu-id="4daf0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4daf0-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest4 -ResourceGroupName psh-test-rg -Location "East US" -Tags @{Test="true";CreationYear="2020"}                                                                                                                                                                                         
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest4
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest4
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest4.us.attest.azure.net
Tags              : {CreationYear, Test}
TagsTable         :
                    Name          Value
                    ============  =====
                    CreationYear  2020
                    Test          true
```

<span data-ttu-id="4daf0-109">Skapa en ny instans av Attesteringsservern med namnet *pshtest4* med ett par Taggar och Använd AAD Trust för att hantera shirt (policy.</span><span class="sxs-lookup"><span data-stu-id="4daf0-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="4daf0-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4daf0-110">Example 2</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg -Location "East US" -PolicySignersCertificateFile .\cert1.pem                                                                                                                                                
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest3
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest3
Status            : Ready
TrustModel        : Isolated
AttestUri         : https://pshtest3.us.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="4daf0-111">Skapa en ny instans av Attesteringsservern med namnet *pshtest3* som använder Isoladed-förtroende för MASTERing shirt (-princip genom att ange en uppsättning betrodda signerings nycklar via en PEM fil.</span><span class="sxs-lookup"><span data-stu-id="4daf0-111">Create a new instance of an Attestation Provider named *pshtest3* \` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="4daf0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4daf0-112">PARAMETERS</span></span>

### <span data-ttu-id="4daf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4daf0-113">-DefaultProfile</span></span>
<span data-ttu-id="4daf0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4daf0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4daf0-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="4daf0-115">-Location</span></span>
<span data-ttu-id="4daf0-116">Anger den Azure-region där du vill skapa en attesterings leverantör.</span><span class="sxs-lookup"><span data-stu-id="4daf0-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="4daf0-117">Använd kommandot Get-AzResourceProvider med parametern ProviderNamespace för att se dina val.</span><span class="sxs-lookup"><span data-stu-id="4daf0-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4daf0-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4daf0-118">-Name</span></span>
<span data-ttu-id="4daf0-119">Anger namnet på den instans som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="4daf0-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="4daf0-120">Namnet kan vara en kombination av bokstäver, siffror och bindestreck.</span><span class="sxs-lookup"><span data-stu-id="4daf0-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="4daf0-121">Namnet måste börja och sluta med en bokstav eller en siffra.</span><span class="sxs-lookup"><span data-stu-id="4daf0-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="4daf0-122">Namnet måste vara globalt unikt.</span><span class="sxs-lookup"><span data-stu-id="4daf0-122">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4daf0-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="4daf0-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="4daf0-124">Anger uppsättningen betrodda signerings nycklar för utgivnings princip i en enda certifikat fil.</span><span class="sxs-lookup"><span data-stu-id="4daf0-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4daf0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4daf0-125">-ResourceGroupName</span></span>
<span data-ttu-id="4daf0-126">Anger namnet på en befintlig resurs grupp där attesteringen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="4daf0-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4daf0-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4daf0-127">-Tag</span></span>
<span data-ttu-id="4daf0-128">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="4daf0-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4daf0-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4daf0-129">-Confirm</span></span>
<span data-ttu-id="4daf0-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4daf0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4daf0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4daf0-131">-WhatIf</span></span>
<span data-ttu-id="4daf0-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4daf0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4daf0-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4daf0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4daf0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4daf0-134">CommonParameters</span></span>
<span data-ttu-id="4daf0-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4daf0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4daf0-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4daf0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4daf0-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4daf0-137">INPUTS</span></span>

### <span data-ttu-id="4daf0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4daf0-138">System.String</span></span>

### <span data-ttu-id="4daf0-139">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="4daf0-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4daf0-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4daf0-140">OUTPUTS</span></span>

### <span data-ttu-id="4daf0-141">Microsoft. Azure. commands. attestering. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="4daf0-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="4daf0-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4daf0-142">NOTES</span></span>

## <span data-ttu-id="4daf0-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4daf0-143">RELATED LINKS</span></span>
