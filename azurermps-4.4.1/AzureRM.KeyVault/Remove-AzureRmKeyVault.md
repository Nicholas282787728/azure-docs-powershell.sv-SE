---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://go.microsoft.com/fwlink/?LinkId=690162
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 2a30a190fbf257142e1c1e4fb4329fd6c4f41e3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583276"
---
# <span data-ttu-id="ff4af-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ff4af-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="ff4af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff4af-102">SYNOPSIS</span></span>
<span data-ttu-id="ff4af-103">Tar bort ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="ff4af-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff4af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff4af-104">SYNTAX</span></span>

### <span data-ttu-id="ff4af-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="ff4af-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff4af-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="ff4af-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff4af-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff4af-107">DESCRIPTION</span></span>
<span data-ttu-id="ff4af-108">Cmdleten **Remove-AzureRmKeyVault** tar bort det angivna Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="ff4af-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="ff4af-109">Dessutom tas alla nycklar och hemligheter bort i den instansen.</span><span class="sxs-lookup"><span data-stu-id="ff4af-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="ff4af-110">Observera att om du anger resurs gruppen som valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="ff4af-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="ff4af-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff4af-111">EXAMPLES</span></span>

### <span data-ttu-id="ff4af-112">Exempel 1: ta bort ett nyckeltal</span><span class="sxs-lookup"><span data-stu-id="ff4af-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="ff4af-113">Det här kommandot tar bort Key-valvet med namnet Contoso03Vault från din nuvarande prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ff4af-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="ff4af-114">Exempel 2: ta bort ett nyckeltal från en angiven resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ff4af-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="ff4af-115">Det här kommandot tar bort Key-valvet med namnet Contoso03Vault från resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ff4af-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="ff4af-116">Om du inte anger namnet på resurs gruppen söker cmdleten efter det namngivna nyckelvärdet att ta bort i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="ff4af-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="ff4af-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff4af-117">PARAMETERS</span></span>

### <span data-ttu-id="ff4af-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ff4af-118">-Force</span></span>
<span data-ttu-id="ff4af-119">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ff4af-119">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="ff4af-120">Denna cmdlet uppmanar dig som standard att bekräfta att du vill ta bort nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="ff4af-120">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="ff4af-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="ff4af-121">-InRemovedState</span></span>
<span data-ttu-id="ff4af-122">Ta bort det tidigare borttagna valvet permanent.</span><span class="sxs-lookup"><span data-stu-id="ff4af-122">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4af-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="ff4af-123">-Location</span></span>
<span data-ttu-id="ff4af-124">Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="ff4af-124">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff4af-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff4af-126">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ff4af-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4af-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ff4af-127">-VaultName</span></span>
<span data-ttu-id="ff4af-128">Anger namnet på det Key-valv som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ff4af-128">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="ff4af-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff4af-129">-Confirm</span></span>
<span data-ttu-id="ff4af-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff4af-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4af-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff4af-131">-WhatIf</span></span>
<span data-ttu-id="ff4af-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff4af-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff4af-133">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff4af-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff4af-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff4af-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4af-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff4af-135">-DefaultProfile</span></span>
<span data-ttu-id="ff4af-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff4af-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff4af-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff4af-137">CommonParameters</span></span>
<span data-ttu-id="ff4af-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff4af-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff4af-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff4af-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff4af-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff4af-140">INPUTS</span></span>

## <span data-ttu-id="ff4af-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff4af-141">OUTPUTS</span></span>

## <span data-ttu-id="ff4af-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff4af-142">NOTES</span></span>

## <span data-ttu-id="ff4af-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff4af-143">RELATED LINKS</span></span>

[<span data-ttu-id="ff4af-144">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ff4af-144">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="ff4af-145">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ff4af-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
