---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 90dade6f8ae40d007e7f5dc575c954b1d4ad639f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319760"
---
# <span data-ttu-id="70152-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="70152-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="70152-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70152-102">SYNOPSIS</span></span>
<span data-ttu-id="70152-103">Hämtar information om en Azure AD-administratör för SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="70152-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="70152-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70152-104">SYNTAX</span></span>

### <span data-ttu-id="70152-105">UseResourceGroupAndInstanceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="70152-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70152-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70152-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70152-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70152-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70152-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70152-108">DESCRIPTION</span></span>
<span data-ttu-id="70152-109">Cmdleten **Get-AzSqlInstanceActiveDirectoryAdministrator** hämtar information om en Azure Active Directory (Azure AD-administratör) för en AzureSQL-hanterad instans i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="70152-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="70152-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70152-110">EXAMPLES</span></span>

### <span data-ttu-id="70152-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="70152-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="70152-112">Med det här kommandot får du information om en Azure AD-administratör för en hanterad instans med namnet ManagedInstance01 som är associerat med en resurs grupp med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="70152-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="70152-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="70152-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="70152-114">Det här kommandot får information om en Azure AD-administratör från ett hanterat instans objekt.</span><span class="sxs-lookup"><span data-stu-id="70152-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="70152-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="70152-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="70152-116">Det här kommandot får information om en Azure AD-administratör med resurs identifieraren för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="70152-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="70152-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70152-117">PARAMETERS</span></span>

### <span data-ttu-id="70152-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70152-118">-DefaultProfile</span></span>
<span data-ttu-id="70152-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70152-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70152-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70152-120">-InputObject</span></span>
<span data-ttu-id="70152-121">Det hanterade instans objekt som ska användas.</span><span class="sxs-lookup"><span data-stu-id="70152-121">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70152-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="70152-122">-InstanceName</span></span>
<span data-ttu-id="70152-123">SQL-hanterat instans namn.</span><span class="sxs-lookup"><span data-stu-id="70152-123">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70152-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70152-124">-ResourceGroupName</span></span>
<span data-ttu-id="70152-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="70152-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70152-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70152-126">-ResourceId</span></span>
<span data-ttu-id="70152-127">ID för den instans som ska användas</span><span class="sxs-lookup"><span data-stu-id="70152-127">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70152-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70152-128">CommonParameters</span></span>
<span data-ttu-id="70152-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70152-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70152-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70152-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70152-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70152-131">INPUTS</span></span>

### <span data-ttu-id="70152-132">System. String</span><span class="sxs-lookup"><span data-stu-id="70152-132">System.String</span></span>

## <span data-ttu-id="70152-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70152-133">OUTPUTS</span></span>

### <span data-ttu-id="70152-134">Microsoft. Azure. commands. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="70152-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="70152-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70152-135">NOTES</span></span>

## <span data-ttu-id="70152-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70152-136">RELATED LINKS</span></span>

[<span data-ttu-id="70152-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="70152-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="70152-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="70152-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
