---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
ms.openlocfilehash: d7bd1e776cc0593f57a17e8d83ecde3f6981973b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929861"
---
# <span data-ttu-id="47828-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="47828-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="47828-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47828-102">SYNOPSIS</span></span>
<span data-ttu-id="47828-103">Återskapar den angivna nyckeln för ett Azure Storage-konto med Key valv.</span><span class="sxs-lookup"><span data-stu-id="47828-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47828-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47828-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47828-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47828-105">DESCRIPTION</span></span>
<span data-ttu-id="47828-106">Återskapar den angivna nyckeln för ett Azure Storage-konto för Key valv som hanteras och anger nyckeln som den aktiva nyckeln.</span><span class="sxs-lookup"><span data-stu-id="47828-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="47828-107">Key valv proxyservrar samtalet till Azure Resource Manager för att återskapa nyckeln.</span><span class="sxs-lookup"><span data-stu-id="47828-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="47828-108">Den som anropar måste Posses behörigheter för att kunna återskapa nycklar på angivet Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="47828-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="47828-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47828-109">EXAMPLES</span></span>

### <span data-ttu-id="47828-110">Exempel 1: återskapa en nyckeln</span><span class="sxs-lookup"><span data-stu-id="47828-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="47828-111">Återskapar ' KEY1 ' för Account ' mystorageaccount ' och anger ' KEY1 ' som aktivt för det Key valv Managed Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="47828-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="47828-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47828-112">PARAMETERS</span></span>

### <span data-ttu-id="47828-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="47828-113">-AccountName</span></span>
<span data-ttu-id="47828-114">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="47828-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="47828-115">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="47828-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47828-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47828-116">-DefaultProfile</span></span>
<span data-ttu-id="47828-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="47828-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47828-118">-Force</span><span class="sxs-lookup"><span data-stu-id="47828-118">-Force</span></span>
<span data-ttu-id="47828-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="47828-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="47828-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="47828-120">-KeyName</span></span>
<span data-ttu-id="47828-121">Namn på lagrings konto nyckeln som ska återskapas och aktive ras.</span><span class="sxs-lookup"><span data-stu-id="47828-121">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47828-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47828-122">-PassThru</span></span>
<span data-ttu-id="47828-123">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="47828-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="47828-124">Om denna växel anges returnerar cmdlet det hanterade lagrings konto som har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="47828-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="47828-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="47828-125">-VaultName</span></span>
<span data-ttu-id="47828-126">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="47828-126">Vault name.</span></span>
<span data-ttu-id="47828-127">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="47828-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="47828-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="47828-128">-Confirm</span></span>
<span data-ttu-id="47828-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="47828-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47828-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47828-130">-WhatIf</span></span>
<span data-ttu-id="47828-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="47828-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47828-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="47828-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47828-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47828-133">CommonParameters</span></span>
<span data-ttu-id="47828-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47828-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47828-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47828-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47828-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47828-136">INPUTS</span></span>

### <span data-ttu-id="47828-137">System. String</span><span class="sxs-lookup"><span data-stu-id="47828-137">System.String</span></span>

## <span data-ttu-id="47828-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47828-138">OUTPUTS</span></span>

### <span data-ttu-id="47828-139">Microsoft. Azure. commands. valv. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47828-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="47828-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47828-140">NOTES</span></span>

## <span data-ttu-id="47828-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47828-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

