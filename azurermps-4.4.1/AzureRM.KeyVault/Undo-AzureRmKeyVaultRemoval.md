---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 57fdddfea449bbde18762afaed0c576c2b4d1db3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756951"
---
# <span data-ttu-id="87e31-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="87e31-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="87e31-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87e31-102">SYNOPSIS</span></span>
<span data-ttu-id="87e31-103">Återställer ett borttaget Key-valv till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="87e31-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87e31-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87e31-104">SYNTAX</span></span>

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87e31-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87e31-105">DESCRIPTION</span></span>
<span data-ttu-id="87e31-106">Med cmdleten **Undo-AzureRmKeyVaultRemoval** återställs ett tidigare borttaget valv.</span><span class="sxs-lookup"><span data-stu-id="87e31-106">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="87e31-107">Det återställda valvet kommer att vara aktivt efter återställning</span><span class="sxs-lookup"><span data-stu-id="87e31-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="87e31-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87e31-108">EXAMPLES</span></span>

### <span data-ttu-id="87e31-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="87e31-109">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="87e31-110">Det här kommandot återställer nyckelordet ' MyKeyVault ' som tidigare tagits bort från eastus2 region och resurs gruppen ' MyResourceGroup ' i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="87e31-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="87e31-111">Den ersätter också taggarna med ny tagg.</span><span class="sxs-lookup"><span data-stu-id="87e31-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="87e31-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87e31-112">PARAMETERS</span></span>

### <span data-ttu-id="87e31-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="87e31-113">-Location</span></span>
<span data-ttu-id="87e31-114">Anger det ursprungliga Azure-området för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="87e31-114">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e31-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e31-115">-ResourceGroupName</span></span>
<span data-ttu-id="87e31-116">Anger namnet på en befintlig resurs grupp där nyckelords valvet ska skapas.</span><span class="sxs-lookup"><span data-stu-id="87e31-116">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e31-117">-Tagg</span><span class="sxs-lookup"><span data-stu-id="87e31-117">-Tag</span></span>
<span data-ttu-id="87e31-118">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="87e31-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="87e31-119">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="87e31-119">For example:</span></span>

<span data-ttu-id="87e31-120">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="87e31-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e31-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="87e31-121">-VaultName</span></span>
<span data-ttu-id="87e31-122">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="87e31-122">Vault name.</span></span>
<span data-ttu-id="87e31-123">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="87e31-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="87e31-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="87e31-124">-Confirm</span></span>
<span data-ttu-id="87e31-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="87e31-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87e31-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87e31-126">-WhatIf</span></span>
<span data-ttu-id="87e31-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="87e31-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87e31-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="87e31-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87e31-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e31-129">-DefaultProfile</span></span>
<span data-ttu-id="87e31-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87e31-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e31-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e31-131">CommonParameters</span></span>
<span data-ttu-id="87e31-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87e31-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e31-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87e31-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e31-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87e31-134">INPUTS</span></span>

### <span data-ttu-id="87e31-135">System. String</span><span class="sxs-lookup"><span data-stu-id="87e31-135">System.String</span></span>
<span data-ttu-id="87e31-136">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="87e31-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="87e31-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87e31-137">OUTPUTS</span></span>

### <span data-ttu-id="87e31-138">Microsoft. Azure. commands. valv. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="87e31-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="87e31-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87e31-139">NOTES</span></span>

## <span data-ttu-id="87e31-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87e31-140">RELATED LINKS</span></span>

[<span data-ttu-id="87e31-141">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="87e31-141">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="87e31-142">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="87e31-142">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="87e31-143">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="87e31-143">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
