---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: abb86f40c9ac4a2ca04e0f14500df6c39e550dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581843"
---
# <span data-ttu-id="0a02e-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="0a02e-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="0a02e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a02e-102">SYNOPSIS</span></span>
<span data-ttu-id="0a02e-103">Lägger till en användare i en grupp.</span><span class="sxs-lookup"><span data-stu-id="0a02e-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a02e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a02e-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a02e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a02e-105">DESCRIPTION</span></span>
<span data-ttu-id="0a02e-106">Cmdleten **Add-AzureRmApiManagementUserToGroup** lägger till en användare i en grupp.</span><span class="sxs-lookup"><span data-stu-id="0a02e-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="0a02e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a02e-107">EXAMPLES</span></span>

### <span data-ttu-id="0a02e-108">Exempel 1: lägga till en användare i en grupp</span><span class="sxs-lookup"><span data-stu-id="0a02e-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="0a02e-109">Det här kommandot lägger till en befintlig användare i en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="0a02e-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="0a02e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a02e-110">PARAMETERS</span></span>

### <span data-ttu-id="0a02e-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0a02e-111">-Context</span></span>
<span data-ttu-id="0a02e-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0a02e-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0a02e-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0a02e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0a02e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a02e-114">-DefaultProfile</span></span>
<span data-ttu-id="0a02e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a02e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a02e-116">-Kund-</span><span class="sxs-lookup"><span data-stu-id="0a02e-116">-GroupId</span></span>
<span data-ttu-id="0a02e-117">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="0a02e-117">Specifies the group ID.</span></span>
<span data-ttu-id="0a02e-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0a02e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0a02e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a02e-119">-PassThru</span></span>
<span data-ttu-id="0a02e-120">passthru</span><span class="sxs-lookup"><span data-stu-id="0a02e-120">passthru</span></span>

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

### <span data-ttu-id="0a02e-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="0a02e-121">-UserId</span></span>
<span data-ttu-id="0a02e-122">Anger användar-ID.</span><span class="sxs-lookup"><span data-stu-id="0a02e-122">Specifies the user ID.</span></span>
<span data-ttu-id="0a02e-123">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0a02e-123">This parameter is required.</span></span>

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

### <span data-ttu-id="0a02e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a02e-124">CommonParameters</span></span>
<span data-ttu-id="0a02e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a02e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a02e-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a02e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a02e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a02e-127">INPUTS</span></span>

### <span data-ttu-id="0a02e-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0a02e-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0a02e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0a02e-129">System.String</span></span>

### <span data-ttu-id="0a02e-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0a02e-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0a02e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a02e-131">OUTPUTS</span></span>

### <span data-ttu-id="0a02e-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0a02e-132">System.Boolean</span></span>

## <span data-ttu-id="0a02e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a02e-133">NOTES</span></span>

## <span data-ttu-id="0a02e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a02e-134">RELATED LINKS</span></span>

[<span data-ttu-id="0a02e-135">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0a02e-135">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="0a02e-136">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="0a02e-136">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


