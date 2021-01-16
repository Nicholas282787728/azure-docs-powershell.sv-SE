---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521993"
---
# <span data-ttu-id="fc345-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="fc345-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="fc345-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc345-102">SYNOPSIS</span></span>
<span data-ttu-id="fc345-103">Återkalla alla användar Delegerings nycklar för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fc345-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="fc345-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc345-104">SYNTAX</span></span>

### <span data-ttu-id="fc345-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="fc345-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc345-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fc345-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc345-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="fc345-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc345-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc345-108">DESCRIPTION</span></span>
<span data-ttu-id="fc345-109">Med cmdleten **REVOKE-AzStorageAccountUserDelegationKeys** kan du återkalla alla användar Delegerings nycklar för ett lagrings konto, så att all ID SAS-token för lagrings kontot också återkallas.</span><span class="sxs-lookup"><span data-stu-id="fc345-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="fc345-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc345-110">EXAMPLES</span></span>

### <span data-ttu-id="fc345-111">Exempel 1: återkalla alla användar Delegerings nycklar för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="fc345-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="fc345-112">I det här exemplet återkallar du alla användar Delegerings nycklar för ett lagrings konto, så att alla identitets-SAS-token som genereras från användar delegering-nycklarna också återkallas.</span><span class="sxs-lookup"><span data-stu-id="fc345-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="fc345-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc345-113">PARAMETERS</span></span>

### <span data-ttu-id="fc345-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc345-114">-DefaultProfile</span></span>
<span data-ttu-id="fc345-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc345-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc345-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc345-116">-InputObject</span></span>
<span data-ttu-id="fc345-117">Ett lagrings konto objekt som returneras av Get_AzStorageAccount, New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="fc345-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc345-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc345-118">-PassThru</span></span>
<span data-ttu-id="fc345-119">Normalt returnerar den här cmdleten inga utdata efter att de upprättats, denna parameter tvingar fram en cmdlet för att returnera ett värde ($true).</span><span class="sxs-lookup"><span data-stu-id="fc345-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="fc345-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc345-120">-ResourceGroupName</span></span>
<span data-ttu-id="fc345-121">Resurs gruppens namn som innehåller lagrings konto resursen.</span><span class="sxs-lookup"><span data-stu-id="fc345-121">The resource group name containing the storage account resource.</span></span>

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

### <span data-ttu-id="fc345-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc345-122">-ResourceId</span></span>
<span data-ttu-id="fc345-123">Resurs-ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fc345-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases: StorageAccountResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc345-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fc345-124">-StorageAccountName</span></span>
<span data-ttu-id="fc345-125">Namnet på lagrings konto resursen.</span><span class="sxs-lookup"><span data-stu-id="fc345-125">The name of the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc345-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fc345-126">-Confirm</span></span>
<span data-ttu-id="fc345-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fc345-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc345-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc345-128">-WhatIf</span></span>
<span data-ttu-id="fc345-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fc345-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc345-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fc345-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc345-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc345-131">CommonParameters</span></span>
<span data-ttu-id="fc345-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc345-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc345-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc345-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc345-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc345-134">INPUTS</span></span>

### <span data-ttu-id="fc345-135">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc345-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="fc345-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fc345-136">System.String</span></span>

## <span data-ttu-id="fc345-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc345-137">OUTPUTS</span></span>

### <span data-ttu-id="fc345-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc345-138">System.Boolean</span></span>

## <span data-ttu-id="fc345-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc345-139">NOTES</span></span>

## <span data-ttu-id="fc345-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc345-140">RELATED LINKS</span></span>
