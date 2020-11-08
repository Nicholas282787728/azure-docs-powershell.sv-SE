---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: bfcb306b12c047c9207e0ef2f1d82bf6eaffc4d3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269476"
---
# <span data-ttu-id="3d61b-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="3d61b-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="3d61b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d61b-102">SYNOPSIS</span></span>
<span data-ttu-id="3d61b-103">Skapar ett konfigurerbart objekt för disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="3d61b-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="3d61b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d61b-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d61b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d61b-105">DESCRIPTION</span></span>
<span data-ttu-id="3d61b-106">Skapar ett konfigurerbart objekt för disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="3d61b-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="3d61b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d61b-107">EXAMPLES</span></span>

### <span data-ttu-id="3d61b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3d61b-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="3d61b-109">Skapar disk krypterings uppsättning med den angivna aktiva knappen i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="3d61b-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="3d61b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d61b-110">PARAMETERS</span></span>

### <span data-ttu-id="3d61b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d61b-111">-DefaultProfile</span></span>
<span data-ttu-id="3d61b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d61b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d61b-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="3d61b-113">-EncryptionType</span></span>
<span data-ttu-id="3d61b-114">Använd det här alternativet för att ange krypterings typ för disk krypterings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="3d61b-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="3d61b-115">Tillgängliga värden är: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '.</span><span class="sxs-lookup"><span data-stu-id="3d61b-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

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

### <span data-ttu-id="3d61b-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3d61b-116">-IdentityType</span></span>
<span data-ttu-id="3d61b-117">Typen av hanterad identitet som används av DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="3d61b-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="3d61b-118">Endast SystemAssigned stöds.</span><span class="sxs-lookup"><span data-stu-id="3d61b-118">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="3d61b-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="3d61b-119">-KeyUrl</span></span>
<span data-ttu-id="3d61b-120">URL som pekar på den aktiva knappen i ett valv</span><span class="sxs-lookup"><span data-stu-id="3d61b-120">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="3d61b-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="3d61b-121">-Location</span></span>
<span data-ttu-id="3d61b-122">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="3d61b-122">Specifies a location.</span></span>

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

### <span data-ttu-id="3d61b-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="3d61b-123">-SourceVaultId</span></span>
<span data-ttu-id="3d61b-124">Resurs-ID för det valv som innehåller den aktiva tangenten.</span><span class="sxs-lookup"><span data-stu-id="3d61b-124">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="3d61b-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3d61b-125">-Tag</span></span>
<span data-ttu-id="3d61b-126">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3d61b-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3d61b-127">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="3d61b-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3d61b-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d61b-128">-Confirm</span></span>
<span data-ttu-id="3d61b-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d61b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d61b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d61b-130">-WhatIf</span></span>
<span data-ttu-id="3d61b-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d61b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d61b-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d61b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d61b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d61b-133">CommonParameters</span></span>
<span data-ttu-id="3d61b-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d61b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d61b-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d61b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d61b-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d61b-136">INPUTS</span></span>

### <span data-ttu-id="3d61b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3d61b-137">System.String</span></span>

### <span data-ttu-id="3d61b-138">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="3d61b-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d61b-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d61b-139">OUTPUTS</span></span>

### <span data-ttu-id="3d61b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3d61b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="3d61b-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d61b-141">NOTES</span></span>

## <span data-ttu-id="3d61b-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d61b-142">RELATED LINKS</span></span>
