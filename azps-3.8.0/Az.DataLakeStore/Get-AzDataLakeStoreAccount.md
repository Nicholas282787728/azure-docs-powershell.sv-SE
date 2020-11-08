---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088232"
---
# <span data-ttu-id="05c99-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05c99-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="05c99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05c99-102">SYNOPSIS</span></span>
<span data-ttu-id="05c99-103">Hämtar information om ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="05c99-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="05c99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05c99-104">SYNTAX</span></span>

### <span data-ttu-id="05c99-105">GetAllInSubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="05c99-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05c99-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="05c99-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05c99-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="05c99-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05c99-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05c99-108">DESCRIPTION</span></span>
<span data-ttu-id="05c99-109">Cmdleten **Get-AzDataLakeStoreAccount** hämtar information om ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="05c99-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="05c99-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05c99-110">EXAMPLES</span></span>

### <span data-ttu-id="05c99-111">Exempel 1: skaffa ett data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="05c99-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="05c99-112">Det här kommandot får kontot ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="05c99-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="05c99-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05c99-113">PARAMETERS</span></span>

### <span data-ttu-id="05c99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c99-114">-DefaultProfile</span></span>
<span data-ttu-id="05c99-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="05c99-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05c99-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="05c99-116">-Name</span></span>
<span data-ttu-id="05c99-117">Anger namnet på kontot som ska visas.</span><span class="sxs-lookup"><span data-stu-id="05c99-117">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05c99-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05c99-118">-ResourceGroupName</span></span>
<span data-ttu-id="05c99-119">Anger namnet på den resurs grupp som innehåller det data Lake Store-konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="05c99-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05c99-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c99-120">CommonParameters</span></span>
<span data-ttu-id="05c99-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05c99-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c99-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05c99-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c99-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05c99-123">INPUTS</span></span>

### <span data-ttu-id="05c99-124">System. String</span><span class="sxs-lookup"><span data-stu-id="05c99-124">System.String</span></span>

## <span data-ttu-id="05c99-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05c99-125">OUTPUTS</span></span>

### <span data-ttu-id="05c99-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05c99-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="05c99-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05c99-127">NOTES</span></span>

## <span data-ttu-id="05c99-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05c99-128">RELATED LINKS</span></span>

[<span data-ttu-id="05c99-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05c99-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="05c99-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05c99-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="05c99-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05c99-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="05c99-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05c99-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


