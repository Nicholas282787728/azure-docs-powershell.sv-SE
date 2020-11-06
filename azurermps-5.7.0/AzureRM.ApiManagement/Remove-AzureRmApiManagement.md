---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 197b1605d178c0aaa1c3f96580cb295306910232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584487"
---
# <span data-ttu-id="3bd1a-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3bd1a-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="3bd1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bd1a-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd1a-103">Tar bort en API-hanterings tjänst.</span><span class="sxs-lookup"><span data-stu-id="3bd1a-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bd1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bd1a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd1a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bd1a-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd1a-106">Cmdleten **Remove-AzureRmApiManagement** tar bort en Azure API Management-tjänst.</span><span class="sxs-lookup"><span data-stu-id="3bd1a-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="3bd1a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bd1a-107">EXAMPLES</span></span>

### <span data-ttu-id="3bd1a-108">Exempel 1: ta bort en API-hanterings tjänst</span><span class="sxs-lookup"><span data-stu-id="3bd1a-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="3bd1a-109">Det här kommandot tar bort API-hanteringskonsolen med namnet ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="3bd1a-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="3bd1a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bd1a-110">PARAMETERS</span></span>

### <span data-ttu-id="3bd1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd1a-111">-DefaultProfile</span></span>
<span data-ttu-id="3bd1a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3bd1a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3bd1a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="3bd1a-113">-Name</span></span>
<span data-ttu-id="3bd1a-114">Anger namnet på den API-hanterings distribution som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="3bd1a-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd1a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bd1a-115">-PassThru</span></span>
<span data-ttu-id="3bd1a-116">Anger att den här cmdleten returnerar ett värde för $True om åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="3bd1a-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="3bd1a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bd1a-117">-ResourceGroupName</span></span>
<span data-ttu-id="3bd1a-118">Anger namnet på den resurs grupp som distributionen av API-hanteringen finns under.</span><span class="sxs-lookup"><span data-stu-id="3bd1a-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd1a-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3bd1a-119">-Confirm</span></span>
<span data-ttu-id="3bd1a-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3bd1a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd1a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd1a-121">-WhatIf</span></span>
<span data-ttu-id="3bd1a-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3bd1a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd1a-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3bd1a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd1a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd1a-124">CommonParameters</span></span>
<span data-ttu-id="3bd1a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bd1a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd1a-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd1a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd1a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bd1a-127">INPUTS</span></span>

### <span data-ttu-id="3bd1a-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="3bd1a-128">None</span></span>
<span data-ttu-id="3bd1a-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3bd1a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3bd1a-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bd1a-130">OUTPUTS</span></span>

### <span data-ttu-id="3bd1a-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3bd1a-131">System.Boolean</span></span>

## <span data-ttu-id="3bd1a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bd1a-132">NOTES</span></span>

## <span data-ttu-id="3bd1a-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bd1a-133">RELATED LINKS</span></span>

[<span data-ttu-id="3bd1a-134">Säkerhets kopiering-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3bd1a-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="3bd1a-135">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3bd1a-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="3bd1a-136">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3bd1a-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="3bd1a-137">Återställ-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3bd1a-137">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


