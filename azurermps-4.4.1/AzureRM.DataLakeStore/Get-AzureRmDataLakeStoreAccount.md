---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c05ca64db5b04ef78778e39d9ae6347db4ca05b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574676"
---
# <span data-ttu-id="dc74b-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dc74b-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="dc74b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc74b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc74b-103">Hämtar information om ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="dc74b-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc74b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc74b-104">SYNTAX</span></span>

### <span data-ttu-id="dc74b-105">Allt i abonnemanget (standard)</span><span class="sxs-lookup"><span data-stu-id="dc74b-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc74b-106">Alla i resurs grupp</span><span class="sxs-lookup"><span data-stu-id="dc74b-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc74b-107">Specifikt konto</span><span class="sxs-lookup"><span data-stu-id="dc74b-107">Specific Account</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc74b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc74b-108">DESCRIPTION</span></span>
<span data-ttu-id="dc74b-109">Cmdleten **Get-AzureRmDataLakeStoreAccount** hämtar information om ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="dc74b-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="dc74b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc74b-110">EXAMPLES</span></span>

### <span data-ttu-id="dc74b-111">Exempel 1: skaffa ett data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="dc74b-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="dc74b-112">Det här kommandot får kontot ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="dc74b-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="dc74b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc74b-113">PARAMETERS</span></span>

### <span data-ttu-id="dc74b-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc74b-114">-Name</span></span>
<span data-ttu-id="dc74b-115">Anger namnet på kontot som ska visas.</span><span class="sxs-lookup"><span data-stu-id="dc74b-115">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc74b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc74b-116">-ResourceGroupName</span></span>
<span data-ttu-id="dc74b-117">Anger namnet på den resurs grupp som innehåller det data Lake Store-konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="dc74b-117">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc74b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc74b-118">-DefaultProfile</span></span>
<span data-ttu-id="dc74b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc74b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc74b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc74b-120">CommonParameters</span></span>
<span data-ttu-id="dc74b-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc74b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc74b-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc74b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc74b-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc74b-123">INPUTS</span></span>

## <span data-ttu-id="dc74b-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc74b-124">OUTPUTS</span></span>

### <span data-ttu-id="dc74b-125">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dc74b-125">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="dc74b-126">Det specifika data Lake Store-kontot som frågade efter.</span><span class="sxs-lookup"><span data-stu-id="dc74b-126">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="dc74b-127">Förteckning<PSDataLakeStoreAccount></span><span class="sxs-lookup"><span data-stu-id="dc74b-127">List<PSDataLakeStoreAccount></span></span>
<span data-ttu-id="dc74b-128">En lista över data Lake Store-konton i resurs gruppen eller abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="dc74b-128">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="dc74b-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc74b-129">NOTES</span></span>

## <span data-ttu-id="dc74b-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc74b-130">RELATED LINKS</span></span>

[<span data-ttu-id="dc74b-131">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dc74b-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="dc74b-132">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dc74b-132">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="dc74b-133">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dc74b-133">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="dc74b-134">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dc74b-134">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


