---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422840"
---
# <span data-ttu-id="0ee11-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="0ee11-101">New-AzAttestation</span></span>

## <span data-ttu-id="0ee11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ee11-102">SYNOPSIS</span></span>
<span data-ttu-id="0ee11-103">Skapar en attestering</span><span class="sxs-lookup"><span data-stu-id="0ee11-103">Creates an attestation</span></span>

## <span data-ttu-id="0ee11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ee11-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ee11-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ee11-105">DESCRIPTION</span></span>
<span data-ttu-id="0ee11-106">New-AzAttestation cmdlet skapar en attestering i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0ee11-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="0ee11-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ee11-107">EXAMPLES</span></span>

### <span data-ttu-id="0ee11-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0ee11-108">Example 1</span></span>
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

<span data-ttu-id="0ee11-109">Skapa en ny instans av Attesteringsservern med namnet *pshtest4* med ett par Taggar och Använd AAD Trust för att hantera shirt (policy.</span><span class="sxs-lookup"><span data-stu-id="0ee11-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="0ee11-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0ee11-110">Example 2</span></span>
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

<span data-ttu-id="0ee11-111">Skapa en ny instans av Attesteringsservern med namnet *pshtest3* som använder Isoladed-förtroende för MASTERing shirt (-princip genom att ange en uppsättning betrodda signerings nycklar via en PEM fil.</span><span class="sxs-lookup"><span data-stu-id="0ee11-111">Create a new instance of an Attestation Provider named *pshtest3*\` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="0ee11-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ee11-112">PARAMETERS</span></span>

### <span data-ttu-id="0ee11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ee11-113">-DefaultProfile</span></span>
<span data-ttu-id="0ee11-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ee11-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ee11-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="0ee11-115">-Location</span></span>
<span data-ttu-id="0ee11-116">Anger den Azure-region där du vill skapa en attesterings leverantör.</span><span class="sxs-lookup"><span data-stu-id="0ee11-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="0ee11-117">Använd kommandot Get-AzResourceProvider med parametern ProviderNamespace för att se dina val.</span><span class="sxs-lookup"><span data-stu-id="0ee11-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="0ee11-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ee11-118">-Name</span></span>
<span data-ttu-id="0ee11-119">Anger namnet på den instans som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0ee11-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="0ee11-120">Namnet kan vara en kombination av bokstäver, siffror och bindestreck.</span><span class="sxs-lookup"><span data-stu-id="0ee11-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="0ee11-121">Namnet måste börja och sluta med en bokstav eller en siffra.</span><span class="sxs-lookup"><span data-stu-id="0ee11-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="0ee11-122">Namnet måste vara globalt unikt.</span><span class="sxs-lookup"><span data-stu-id="0ee11-122">The name must be universally unique.</span></span>

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

### <span data-ttu-id="0ee11-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="0ee11-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="0ee11-124">Anger uppsättningen betrodda signerings nycklar för utgivnings princip i en enda certifikat fil.</span><span class="sxs-lookup"><span data-stu-id="0ee11-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

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

### <span data-ttu-id="0ee11-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ee11-125">-ResourceGroupName</span></span>
<span data-ttu-id="0ee11-126">Anger namnet på en befintlig resurs grupp där attesteringen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0ee11-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

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

### <span data-ttu-id="0ee11-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0ee11-127">-Tag</span></span>
<span data-ttu-id="0ee11-128">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="0ee11-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="0ee11-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0ee11-129">-Confirm</span></span>
<span data-ttu-id="0ee11-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0ee11-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ee11-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ee11-131">-WhatIf</span></span>
<span data-ttu-id="0ee11-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0ee11-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ee11-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0ee11-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ee11-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ee11-134">CommonParameters</span></span>
<span data-ttu-id="0ee11-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ee11-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ee11-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ee11-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ee11-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ee11-137">INPUTS</span></span>

### <span data-ttu-id="0ee11-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0ee11-138">System.String</span></span>

### <span data-ttu-id="0ee11-139">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="0ee11-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0ee11-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ee11-140">OUTPUTS</span></span>

### <span data-ttu-id="0ee11-141">Microsoft. Azure. commands. attestering. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="0ee11-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="0ee11-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ee11-142">NOTES</span></span>

## <span data-ttu-id="0ee11-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ee11-143">RELATED LINKS</span></span>
