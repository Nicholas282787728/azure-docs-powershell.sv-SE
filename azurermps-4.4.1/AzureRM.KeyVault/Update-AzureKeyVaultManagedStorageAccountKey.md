---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 94e1b297879e31ff42f9c12c0e4ad4a601e5e163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582388"
---
# <span data-ttu-id="643c4-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="643c4-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="643c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="643c4-102">SYNOPSIS</span></span>
<span data-ttu-id="643c4-103">Återskapar den angivna nyckeln för ett Azure Storage-konto med Key valv.</span><span class="sxs-lookup"><span data-stu-id="643c4-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="643c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="643c4-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="643c4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="643c4-105">DESCRIPTION</span></span>
<span data-ttu-id="643c4-106">Återskapar den angivna nyckeln för ett Azure Storage-konto för Key valv som hanteras och anger nyckeln som den aktiva nyckeln.</span><span class="sxs-lookup"><span data-stu-id="643c4-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="643c4-107">Key valv proxyservrar samtalet till Azure Resource Manager för att återskapa nyckeln.</span><span class="sxs-lookup"><span data-stu-id="643c4-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="643c4-108">Den som anropar måste Posses behörigheter för att kunna återskapa nycklar på angivet Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="643c4-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="643c4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="643c4-109">EXAMPLES</span></span>

### <span data-ttu-id="643c4-110">Exempel 1: återskapa en nyckeln</span><span class="sxs-lookup"><span data-stu-id="643c4-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="643c4-111">Återskapar ' KEY1 ' för Account ' mystorageaccount ' och anger ' KEY1 ' som aktivt för det Key valv Managed Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="643c4-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="643c4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="643c4-112">PARAMETERS</span></span>

### <span data-ttu-id="643c4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="643c4-113">-AccountName</span></span>
<span data-ttu-id="643c4-114">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="643c4-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="643c4-115">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="643c4-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="643c4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="643c4-116">-Force</span></span>
<span data-ttu-id="643c4-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="643c4-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="643c4-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="643c4-118">-KeyName</span></span>
<span data-ttu-id="643c4-119">Namn på lagrings konto nyckeln som ska återskapas och aktive ras.</span><span class="sxs-lookup"><span data-stu-id="643c4-119">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="643c4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="643c4-120">-PassThru</span></span>
<span data-ttu-id="643c4-121">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="643c4-121">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="643c4-122">Om denna växel anges returnerar cmdlet det hanterade lagrings konto som har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="643c4-122">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="643c4-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="643c4-123">-VaultName</span></span>
<span data-ttu-id="643c4-124">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="643c4-124">Vault name.</span></span>
<span data-ttu-id="643c4-125">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="643c4-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="643c4-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="643c4-126">-Confirm</span></span>
<span data-ttu-id="643c4-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="643c4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="643c4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="643c4-128">-WhatIf</span></span>
<span data-ttu-id="643c4-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="643c4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="643c4-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="643c4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="643c4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="643c4-131">-DefaultProfile</span></span>
<span data-ttu-id="643c4-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="643c4-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="643c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="643c4-133">CommonParameters</span></span>
<span data-ttu-id="643c4-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="643c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="643c4-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="643c4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="643c4-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="643c4-136">INPUTS</span></span>

### <span data-ttu-id="643c4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="643c4-137">System.String</span></span>

## <span data-ttu-id="643c4-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="643c4-138">OUTPUTS</span></span>

### <span data-ttu-id="643c4-139">Microsoft. Azure. commands. valv. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="643c4-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="643c4-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="643c4-140">NOTES</span></span>

## <span data-ttu-id="643c4-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="643c4-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

