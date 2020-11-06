---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 61899a50c857fc3e8852d362d5905b0ca2fedf6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579567"
---
# <span data-ttu-id="fdf9d-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fdf9d-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="fdf9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fdf9d-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf9d-103">Hämtar information om ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="fdf9d-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdf9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fdf9d-104">SYNTAX</span></span>

### <span data-ttu-id="fdf9d-105">GetAllInSubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="fdf9d-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdf9d-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fdf9d-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdf9d-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="fdf9d-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf9d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fdf9d-108">DESCRIPTION</span></span>
<span data-ttu-id="fdf9d-109">Cmdleten **Get-AzureRmDataLakeStoreAccount** hämtar information om ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="fdf9d-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="fdf9d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fdf9d-110">EXAMPLES</span></span>

### <span data-ttu-id="fdf9d-111">Exempel 1: skaffa ett data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="fdf9d-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="fdf9d-112">Det här kommandot får kontot ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="fdf9d-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="fdf9d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fdf9d-113">PARAMETERS</span></span>

### <span data-ttu-id="fdf9d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf9d-114">-DefaultProfile</span></span>
<span data-ttu-id="fdf9d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fdf9d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdf9d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="fdf9d-116">-Name</span></span>
<span data-ttu-id="fdf9d-117">Anger namnet på kontot som ska visas.</span><span class="sxs-lookup"><span data-stu-id="fdf9d-117">Specifies the name of the account to get.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf9d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf9d-118">-ResourceGroupName</span></span>
<span data-ttu-id="fdf9d-119">Anger namnet på den resurs grupp som innehåller det data Lake Store-konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="fdf9d-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf9d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf9d-120">CommonParameters</span></span>
<span data-ttu-id="fdf9d-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf9d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf9d-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf9d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf9d-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fdf9d-123">INPUTS</span></span>

### <span data-ttu-id="fdf9d-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="fdf9d-124">None</span></span>
<span data-ttu-id="fdf9d-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="fdf9d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fdf9d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fdf9d-126">OUTPUTS</span></span>

### <span data-ttu-id="fdf9d-127">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fdf9d-127">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="fdf9d-128">Det specifika data Lake Store-kontot som frågade efter.</span><span class="sxs-lookup"><span data-stu-id="fdf9d-128">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="fdf9d-129">Förteckning<PSDataLakeStoreAccountBasic></span><span class="sxs-lookup"><span data-stu-id="fdf9d-129">List<PSDataLakeStoreAccountBasic></span></span>
<span data-ttu-id="fdf9d-130">En lista över data Lake Store-konton i resurs gruppen eller abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fdf9d-130">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="fdf9d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fdf9d-131">NOTES</span></span>

## <span data-ttu-id="fdf9d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fdf9d-132">RELATED LINKS</span></span>

[<span data-ttu-id="fdf9d-133">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fdf9d-133">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="fdf9d-134">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fdf9d-134">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="fdf9d-135">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fdf9d-135">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="fdf9d-136">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fdf9d-136">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


