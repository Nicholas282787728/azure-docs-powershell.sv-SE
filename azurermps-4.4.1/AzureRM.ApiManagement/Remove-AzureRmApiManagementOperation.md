---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 685da9955f272066ec39890ea0f3a063d3b2f9b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574751"
---
# <span data-ttu-id="2c576-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2c576-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="2c576-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c576-102">SYNOPSIS</span></span>
<span data-ttu-id="2c576-103">Tar bort en befintlig åtgärd.</span><span class="sxs-lookup"><span data-stu-id="2c576-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c576-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c576-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c576-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c576-105">DESCRIPTION</span></span>
<span data-ttu-id="2c576-106">Cmdleten **Remove-AzureRmApiManagementOperation** tar bort en befintlig åtgärd.</span><span class="sxs-lookup"><span data-stu-id="2c576-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="2c576-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c576-107">EXAMPLES</span></span>

### <span data-ttu-id="2c576-108">Exempel 1: ta bort en befintlig API-åtgärd</span><span class="sxs-lookup"><span data-stu-id="2c576-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>Remove-AzureRmApiManagementOperation -Context $APImContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="2c576-109">Det här kommandot tar bort en befintlig API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="2c576-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="2c576-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c576-110">PARAMETERS</span></span>

### <span data-ttu-id="2c576-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2c576-111">-ApiId</span></span>
<span data-ttu-id="2c576-112">Anger API-identifierare.</span><span class="sxs-lookup"><span data-stu-id="2c576-112">Specifies the identifier of the API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c576-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2c576-113">-Context</span></span>
<span data-ttu-id="2c576-114">Anger en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="2c576-114">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c576-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="2c576-115">-OperationId</span></span>
<span data-ttu-id="2c576-116">Anger API-funktionens identifierare.</span><span class="sxs-lookup"><span data-stu-id="2c576-116">Specifies the identifier of the API operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c576-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c576-117">-PassThru</span></span>
<span data-ttu-id="2c576-118">Anger att denna cmdlet returnerar ett värde för $True om det lyckas, eller ett $False värde.</span><span class="sxs-lookup"><span data-stu-id="2c576-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c576-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c576-119">-Confirm</span></span>
<span data-ttu-id="2c576-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c576-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c576-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c576-121">-WhatIf</span></span>
<span data-ttu-id="2c576-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c576-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c576-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c576-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c576-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c576-124">-DefaultProfile</span></span>
<span data-ttu-id="2c576-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c576-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c576-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c576-126">CommonParameters</span></span>
<span data-ttu-id="2c576-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c576-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c576-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c576-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c576-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c576-129">INPUTS</span></span>

## <span data-ttu-id="2c576-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c576-130">OUTPUTS</span></span>

### <span data-ttu-id="2c576-131">bool</span><span class="sxs-lookup"><span data-stu-id="2c576-131">bool</span></span>

## <span data-ttu-id="2c576-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c576-132">NOTES</span></span>

## <span data-ttu-id="2c576-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c576-133">RELATED LINKS</span></span>

[<span data-ttu-id="2c576-134">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2c576-134">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="2c576-135">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2c576-135">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="2c576-136">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="2c576-136">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


