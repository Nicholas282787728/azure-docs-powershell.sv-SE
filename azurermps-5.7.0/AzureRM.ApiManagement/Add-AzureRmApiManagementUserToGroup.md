---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: 300c99926ae7f58a6bf53ba49f3b5b86f243e150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756824"
---
# <span data-ttu-id="cc221-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="cc221-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="cc221-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc221-102">SYNOPSIS</span></span>
<span data-ttu-id="cc221-103">Lägger till en användare i en grupp.</span><span class="sxs-lookup"><span data-stu-id="cc221-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc221-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc221-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc221-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc221-105">DESCRIPTION</span></span>
<span data-ttu-id="cc221-106">Cmdleten **Add-AzureRmApiManagementUserToGroup** lägger till en användare i en grupp.</span><span class="sxs-lookup"><span data-stu-id="cc221-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="cc221-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc221-107">EXAMPLES</span></span>

### <span data-ttu-id="cc221-108">Exempel 1: lägga till en användare i en grupp</span><span class="sxs-lookup"><span data-stu-id="cc221-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="cc221-109">Det här kommandot lägger till en befintlig användare i en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="cc221-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="cc221-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc221-110">PARAMETERS</span></span>

### <span data-ttu-id="cc221-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="cc221-111">-Context</span></span>
<span data-ttu-id="cc221-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="cc221-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="cc221-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="cc221-113">This parameter is required.</span></span>

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

### <span data-ttu-id="cc221-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc221-114">-DefaultProfile</span></span>
<span data-ttu-id="cc221-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc221-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="cc221-116">-Kund-</span><span class="sxs-lookup"><span data-stu-id="cc221-116">-GroupId</span></span>
<span data-ttu-id="cc221-117">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="cc221-117">Specifies the group ID.</span></span>
<span data-ttu-id="cc221-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="cc221-118">This parameter is required.</span></span>

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

### <span data-ttu-id="cc221-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc221-119">-PassThru</span></span>
<span data-ttu-id="cc221-120">passthru</span><span class="sxs-lookup"><span data-stu-id="cc221-120">passthru</span></span>

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

### <span data-ttu-id="cc221-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="cc221-121">-UserId</span></span>
<span data-ttu-id="cc221-122">Anger användar-ID.</span><span class="sxs-lookup"><span data-stu-id="cc221-122">Specifies the user ID.</span></span>
<span data-ttu-id="cc221-123">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="cc221-123">This parameter is required.</span></span>

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

### <span data-ttu-id="cc221-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc221-124">CommonParameters</span></span>
<span data-ttu-id="cc221-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc221-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc221-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc221-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc221-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc221-127">INPUTS</span></span>

### <span data-ttu-id="cc221-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="cc221-128">None</span></span>
<span data-ttu-id="cc221-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="cc221-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc221-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc221-130">OUTPUTS</span></span>

### <span data-ttu-id="cc221-131">Returtyp</span><span class="sxs-lookup"><span data-stu-id="cc221-131">Boolean</span></span>

## <span data-ttu-id="cc221-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc221-132">NOTES</span></span>

## <span data-ttu-id="cc221-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc221-133">RELATED LINKS</span></span>

[<span data-ttu-id="cc221-134">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="cc221-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="cc221-135">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="cc221-135">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


