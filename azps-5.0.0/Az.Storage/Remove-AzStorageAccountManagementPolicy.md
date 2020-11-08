---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 6f4907f9ee94c05161fa602fc5cefd0ead4f6224
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272557"
---
# <span data-ttu-id="fb7a2-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fb7a2-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="fb7a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb7a2-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7a2-103">Tar bort hanterings principen för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="fb7a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb7a2-104">SYNTAX</span></span>

### <span data-ttu-id="fb7a2-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="fb7a2-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7a2-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fb7a2-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7a2-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7a2-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7a2-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="fb7a2-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb7a2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb7a2-109">DESCRIPTION</span></span>
<span data-ttu-id="fb7a2-110">Cmdleten **Remove-AzStorageAccountManagementPolicy** tar bort hanterings principen för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="fb7a2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb7a2-111">EXAMPLES</span></span>

### <span data-ttu-id="fb7a2-112">Exempel 1: ta bort hanterings principen för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="fb7a2-113">Det här kommandot tar bort hanterings principen för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="fb7a2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb7a2-114">PARAMETERS</span></span>

### <span data-ttu-id="fb7a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7a2-115">-DefaultProfile</span></span>
<span data-ttu-id="fb7a2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb7a2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb7a2-117">-InputObject</span></span>
<span data-ttu-id="fb7a2-118">Management-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="fb7a2-118">Management Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: PolicyObject
Aliases: ManagementPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7a2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb7a2-119">-PassThru</span></span>
<span data-ttu-id="fb7a2-120">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="fb7a2-121">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="fb7a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb7a2-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7a2-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb7a2-124">-StorageAccount</span></span>
<span data-ttu-id="fb7a2-125">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="fb7a2-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7a2-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fb7a2-126">-StorageAccountName</span></span>
<span data-ttu-id="fb7a2-127">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7a2-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7a2-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="fb7a2-129">Resurs-ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-129">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7a2-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb7a2-130">-Confirm</span></span>
<span data-ttu-id="fb7a2-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb7a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb7a2-132">-WhatIf</span></span>
<span data-ttu-id="fb7a2-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb7a2-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb7a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7a2-135">CommonParameters</span></span>
<span data-ttu-id="fb7a2-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7a2-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb7a2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7a2-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb7a2-138">INPUTS</span></span>

### <span data-ttu-id="fb7a2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fb7a2-139">System.String</span></span>

## <span data-ttu-id="fb7a2-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb7a2-140">OUTPUTS</span></span>

### <span data-ttu-id="fb7a2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb7a2-141">System.Boolean</span></span>

## <span data-ttu-id="fb7a2-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb7a2-142">NOTES</span></span>

## <span data-ttu-id="fb7a2-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb7a2-143">RELATED LINKS</span></span>
