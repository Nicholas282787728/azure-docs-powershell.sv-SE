---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 20187e2d7a844b472217fd30acbac9805e85ad40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924458"
---
# <span data-ttu-id="efe9c-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="efe9c-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="efe9c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="efe9c-102">SYNOPSIS</span></span>
<span data-ttu-id="efe9c-103">Tar bort ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="efe9c-103">Deletes a key vault.</span></span>

## <span data-ttu-id="efe9c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="efe9c-104">SYNTAX</span></span>

### <span data-ttu-id="efe9c-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="efe9c-105">ByAvailableVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efe9c-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="efe9c-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efe9c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="efe9c-107">DESCRIPTION</span></span>
<span data-ttu-id="efe9c-108">Cmdleten **Remove-AzKeyVault** tar bort det angivna Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="efe9c-108">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="efe9c-109">Dessutom tas alla nycklar och hemligheter bort i den instansen.</span><span class="sxs-lookup"><span data-stu-id="efe9c-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="efe9c-110">Observera att om du anger resurs gruppen som valfri för denna cmdlet bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="efe9c-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="efe9c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="efe9c-111">EXAMPLES</span></span>

### <span data-ttu-id="efe9c-112">Exempel 1: ta bort ett nyckeltal</span><span class="sxs-lookup"><span data-stu-id="efe9c-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="efe9c-113">Det här kommandot tar bort Key-valvet med namnet Contoso03Vault från din nuvarande prenumeration.</span><span class="sxs-lookup"><span data-stu-id="efe9c-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="efe9c-114">Exempel 2: ta bort ett nyckeltal från en angiven resurs grupp</span><span class="sxs-lookup"><span data-stu-id="efe9c-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="efe9c-115">Det här kommandot tar bort Key-valvet med namnet Contoso03Vault från resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="efe9c-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="efe9c-116">Om du inte anger namnet på resurs gruppen söker cmdleten efter det namngivna nyckelvärdet att ta bort i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="efe9c-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="efe9c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="efe9c-117">PARAMETERS</span></span>

### <span data-ttu-id="efe9c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efe9c-118">-AsJob</span></span>
<span data-ttu-id="efe9c-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="efe9c-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe9c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe9c-120">-DefaultProfile</span></span>
<span data-ttu-id="efe9c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="efe9c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe9c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="efe9c-122">-Force</span></span>
<span data-ttu-id="efe9c-123">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="efe9c-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="efe9c-124">Denna cmdlet uppmanar dig som standard att bekräfta att du vill ta bort nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="efe9c-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe9c-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="efe9c-125">-InRemovedState</span></span>
<span data-ttu-id="efe9c-126">Ta bort det tidigare borttagna valvet permanent.</span><span class="sxs-lookup"><span data-stu-id="efe9c-126">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe9c-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="efe9c-127">-Location</span></span>
<span data-ttu-id="efe9c-128">Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="efe9c-128">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe9c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efe9c-129">-ResourceGroupName</span></span>
<span data-ttu-id="efe9c-130">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="efe9c-130">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe9c-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="efe9c-131">-VaultName</span></span>
<span data-ttu-id="efe9c-132">Anger namnet på det Key-valv som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="efe9c-132">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe9c-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="efe9c-133">-Confirm</span></span>
<span data-ttu-id="efe9c-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="efe9c-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe9c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efe9c-135">-WhatIf</span></span>
<span data-ttu-id="efe9c-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="efe9c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efe9c-137">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="efe9c-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efe9c-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="efe9c-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe9c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe9c-139">CommonParameters</span></span>
<span data-ttu-id="efe9c-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efe9c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe9c-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efe9c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe9c-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="efe9c-142">INPUTS</span></span>

### <span data-ttu-id="efe9c-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="efe9c-143">None</span></span>
<span data-ttu-id="efe9c-144">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="efe9c-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="efe9c-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="efe9c-145">OUTPUTS</span></span>

## <span data-ttu-id="efe9c-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="efe9c-146">NOTES</span></span>

## <span data-ttu-id="efe9c-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="efe9c-147">RELATED LINKS</span></span>

[<span data-ttu-id="efe9c-148">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="efe9c-148">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="efe9c-149">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="efe9c-149">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
