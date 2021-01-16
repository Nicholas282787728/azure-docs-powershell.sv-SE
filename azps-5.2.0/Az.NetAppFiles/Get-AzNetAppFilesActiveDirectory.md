---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 6c082d2e61f81c4e0b8cf9bebefd623584fac3e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410840"
---
# <span data-ttu-id="30ce6-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="30ce6-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="30ce6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="30ce6-103">Hämtar information om en Azure NetApp-fil (ANF) Active Directory-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="30ce6-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="30ce6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30ce6-104">SYNTAX</span></span>

### <span data-ttu-id="30ce6-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="30ce6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30ce6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30ce6-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30ce6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30ce6-107">DESCRIPTION</span></span>
<span data-ttu-id="30ce6-108">Cmdleten **Get-AzNetAppFilesActiveDirectory** hämtar information om en Active Directory-konfiguration för ANF-konton.</span><span class="sxs-lookup"><span data-stu-id="30ce6-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="30ce6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30ce6-109">EXAMPLES</span></span>

### <span data-ttu-id="30ce6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="30ce6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="30ce6-111">Det här kommandot får AD-konfigurationen med namnet MyADConfigName för Azure NetApp-kontot (ANF) med namnet MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="30ce6-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="30ce6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30ce6-112">PARAMETERS</span></span>

### <span data-ttu-id="30ce6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="30ce6-113">-AccountName</span></span>
<span data-ttu-id="30ce6-114">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="30ce6-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ce6-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="30ce6-115">-AccountObject</span></span>
<span data-ttu-id="30ce6-116">Kontot för det nya Active Directory-objektet</span><span class="sxs-lookup"><span data-stu-id="30ce6-116">The Account for the new Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30ce6-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="30ce6-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="30ce6-118">ActiveDirectoryId för ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="30ce6-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActiveDirectoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ce6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ce6-119">-DefaultProfile</span></span>
<span data-ttu-id="30ce6-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30ce6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30ce6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30ce6-121">-ResourceGroupName</span></span>
<span data-ttu-id="30ce6-122">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="30ce6-122">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ce6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ce6-123">CommonParameters</span></span>
<span data-ttu-id="30ce6-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30ce6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ce6-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30ce6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ce6-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30ce6-126">INPUTS</span></span>

### <span data-ttu-id="30ce6-127">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="30ce6-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="30ce6-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30ce6-128">OUTPUTS</span></span>

### <span data-ttu-id="30ce6-129">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="30ce6-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="30ce6-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30ce6-130">NOTES</span></span>

## <span data-ttu-id="30ce6-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30ce6-131">RELATED LINKS</span></span>
