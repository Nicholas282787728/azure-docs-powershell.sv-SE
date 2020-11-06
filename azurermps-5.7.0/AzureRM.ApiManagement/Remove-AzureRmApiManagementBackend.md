---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 347a05c5e197a93458a64c4079ce1fd430e631f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577280"
---
# <span data-ttu-id="d264d-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d264d-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="d264d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d264d-102">SYNOPSIS</span></span>
<span data-ttu-id="d264d-103">Tar bort en server del.</span><span class="sxs-lookup"><span data-stu-id="d264d-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d264d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d264d-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d264d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d264d-105">DESCRIPTION</span></span>
<span data-ttu-id="d264d-106">Tar bort en server del som anges av identifieraren från API-hanteringen.</span><span class="sxs-lookup"><span data-stu-id="d264d-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="d264d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d264d-107">EXAMPLES</span></span>

### <span data-ttu-id="d264d-108">Exempel 1: ta bort Server delen 123</span><span class="sxs-lookup"><span data-stu-id="d264d-108">Example 1: Remove the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="d264d-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d264d-109">PARAMETERS</span></span>

### <span data-ttu-id="d264d-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="d264d-110">-BackendId</span></span>
<span data-ttu-id="d264d-111">Identifierare för befintlig server del.</span><span class="sxs-lookup"><span data-stu-id="d264d-111">Identifier of existing backend.</span></span>
<span data-ttu-id="d264d-112">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d264d-112">This parameter is required.</span></span>

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

### <span data-ttu-id="d264d-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d264d-113">-Context</span></span>
<span data-ttu-id="d264d-114">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d264d-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d264d-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d264d-115">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d264d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d264d-116">-DefaultProfile</span></span>
<span data-ttu-id="d264d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d264d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d264d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d264d-118">-PassThru</span></span>
<span data-ttu-id="d264d-119">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="d264d-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d264d-120">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d264d-120">This parameter is optional.</span></span>
<span data-ttu-id="d264d-121">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="d264d-121">Default value is false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d264d-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d264d-122">-Confirm</span></span>
<span data-ttu-id="d264d-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d264d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d264d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d264d-124">-WhatIf</span></span>
<span data-ttu-id="d264d-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d264d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d264d-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d264d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d264d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d264d-127">CommonParameters</span></span>
<span data-ttu-id="d264d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d264d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d264d-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d264d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d264d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d264d-130">INPUTS</span></span>

### <span data-ttu-id="d264d-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="d264d-131">None</span></span>
<span data-ttu-id="d264d-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d264d-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d264d-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d264d-133">OUTPUTS</span></span>

### <span data-ttu-id="d264d-134">bool</span><span class="sxs-lookup"><span data-stu-id="d264d-134">bool</span></span>

## <span data-ttu-id="d264d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d264d-135">NOTES</span></span>

## <span data-ttu-id="d264d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d264d-136">RELATED LINKS</span></span>

[<span data-ttu-id="d264d-137">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d264d-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="d264d-138">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d264d-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d264d-139">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d264d-139">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="d264d-140">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d264d-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="d264d-141">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d264d-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
