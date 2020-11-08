---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 5d38a1104d1f2d1f569560027c540a2c8605bdae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089193"
---
# <span data-ttu-id="1986e-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="1986e-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="1986e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1986e-102">SYNOPSIS</span></span>
<span data-ttu-id="1986e-103">Skapar ett konfigurerbart objekt för disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="1986e-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="1986e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1986e-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1986e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1986e-105">DESCRIPTION</span></span>
<span data-ttu-id="1986e-106">Skapar ett konfigurerbart objekt för disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="1986e-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="1986e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1986e-107">EXAMPLES</span></span>

### <span data-ttu-id="1986e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1986e-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="1986e-109">Skapar disk krypterings uppsättning med den angivna aktiva knappen i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="1986e-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="1986e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1986e-110">PARAMETERS</span></span>

### <span data-ttu-id="1986e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1986e-111">-DefaultProfile</span></span>
<span data-ttu-id="1986e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1986e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1986e-113">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="1986e-113">-IdentityType</span></span>
<span data-ttu-id="1986e-114">Typen av hanterad identitet som används av DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="1986e-114">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="1986e-115">Endast SystemAssigned stöds.</span><span class="sxs-lookup"><span data-stu-id="1986e-115">Only SystemAssigned is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1986e-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="1986e-116">-KeyUrl</span></span>
<span data-ttu-id="1986e-117">URL som pekar på den aktiva knappen i ett valv</span><span class="sxs-lookup"><span data-stu-id="1986e-117">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="1986e-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="1986e-118">-Location</span></span>
<span data-ttu-id="1986e-119">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="1986e-119">Specifies a location.</span></span>

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

### <span data-ttu-id="1986e-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="1986e-120">-SourceVaultId</span></span>
<span data-ttu-id="1986e-121">Resurs-ID för det valv som innehåller den aktiva tangenten.</span><span class="sxs-lookup"><span data-stu-id="1986e-121">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1986e-122">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1986e-122">-Tag</span></span>
<span data-ttu-id="1986e-123">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1986e-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1986e-124">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="1986e-124">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1986e-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1986e-125">-Confirm</span></span>
<span data-ttu-id="1986e-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1986e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1986e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1986e-127">-WhatIf</span></span>
<span data-ttu-id="1986e-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1986e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1986e-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1986e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1986e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1986e-130">CommonParameters</span></span>
<span data-ttu-id="1986e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1986e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1986e-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1986e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1986e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1986e-133">INPUTS</span></span>

### <span data-ttu-id="1986e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1986e-134">System.String</span></span>

### <span data-ttu-id="1986e-135">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="1986e-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1986e-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1986e-136">OUTPUTS</span></span>

### <span data-ttu-id="1986e-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1986e-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="1986e-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1986e-138">NOTES</span></span>

## <span data-ttu-id="1986e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1986e-139">RELATED LINKS</span></span>
