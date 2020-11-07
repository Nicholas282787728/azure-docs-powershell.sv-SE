---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: d3e7a04f292be8e83bc28456c0510450c078a777
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931106"
---
# <span data-ttu-id="96632-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96632-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="96632-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96632-102">SYNOPSIS</span></span>
<span data-ttu-id="96632-103">Tar bort ett lagrings konto från Azure.</span><span class="sxs-lookup"><span data-stu-id="96632-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96632-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96632-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96632-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96632-105">DESCRIPTION</span></span>
<span data-ttu-id="96632-106">Cmdleten **Remove-AzureRmStorageAccount** tar bort ett lagrings konto från Azure.</span><span class="sxs-lookup"><span data-stu-id="96632-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="96632-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96632-107">EXAMPLES</span></span>

### <span data-ttu-id="96632-108">Exempel 1: ta bort ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="96632-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="96632-109">Det här kommandot tar bort det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="96632-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="96632-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96632-110">PARAMETERS</span></span>

### <span data-ttu-id="96632-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96632-111">-AsJob</span></span>
<span data-ttu-id="96632-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="96632-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96632-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96632-113">-DefaultProfile</span></span>
<span data-ttu-id="96632-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96632-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96632-115">-Force</span><span class="sxs-lookup"><span data-stu-id="96632-115">-Force</span></span>
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

### <span data-ttu-id="96632-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="96632-116">-Name</span></span>
<span data-ttu-id="96632-117">Anger namnet på det lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="96632-117">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96632-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96632-118">-ResourceGroupName</span></span>
<span data-ttu-id="96632-119">Anger namnet på den resurs grupp som innehåller det lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="96632-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="96632-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96632-120">-Confirm</span></span>
<span data-ttu-id="96632-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96632-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96632-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96632-122">-WhatIf</span></span>
<span data-ttu-id="96632-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96632-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96632-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96632-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96632-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96632-125">CommonParameters</span></span>
<span data-ttu-id="96632-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96632-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96632-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96632-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96632-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96632-128">INPUTS</span></span>

### <span data-ttu-id="96632-129">System. String</span><span class="sxs-lookup"><span data-stu-id="96632-129">System.String</span></span>

## <span data-ttu-id="96632-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96632-130">OUTPUTS</span></span>

### <span data-ttu-id="96632-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="96632-131">System.Void</span></span>

## <span data-ttu-id="96632-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96632-132">NOTES</span></span>

## <span data-ttu-id="96632-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96632-133">RELATED LINKS</span></span>

[<span data-ttu-id="96632-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96632-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="96632-135">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96632-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="96632-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96632-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


